<!-- POSTS THAT NEED LOVE -->
<script type="text/discourse-plugin" version="0.8.18">
   if (I18n.translations.en) {
        I18n.translations.en.js.filters.needsreply = { title: "Posts That Need Love", help: "Topics that need more replies." };
    }

    // Add active class to Needs Reply button
    api.modifyClass('component:navigation-item', {
        active: Ember.computed("contentFilterMode", "filterMode", function() {
            let contentFilterMode = this.get('content').get('filterMode');
            if (window.location.search === "?ascending=true&order=posts&max_posts=5") {
                return contentFilterMode === "needsreply";
            } else {
                return this._super(contentFilterMode, this.get('filterMode'));
            }
       }),
    });

    // Remove max_posts filter
    api.modifyClass('controller:discovery/topics', {
        resetParams: function () {
            this.setProperties({max_posts: null});
            this._super();
        }
    });

    Discourse.ExternalNavItem = Discourse.NavItem.extend({
        href: function () {
            return this.get('href');
        }.property("href")
    });

    Discourse.NavItem.reopenClass({
        buildList: function(category, args) {
            let list = this._super(category, args);

            // Exclude certain categories from showing needs_reply
            excludeList = ['process', 'resources', 'prompts', 'staff', 'unpublished-prompts'];

            if(!category) {
                // does not have a category
                // if there's no tag, do nothing
                if (!args.tagId) {}
                //there is a tag, build the url with the tagId, but without the category
                else {
                  list.push(Discourse.ExternalNavItem.create({href: '/tags/' + args.tagId  + '?ascending=true&order=posts&max_posts=5', name: 'needsreply'}));
                }

            } else if (!category.parentCategory) {
                // is not a sub-category
                if (excludeList.indexOf(category.slug) != -1) {
                  // in the exclude list, do nothing
                } else {
                    // if there's no tag, build url without tagId
                    if (!args.tagId) {
                      list.push(Discourse.ExternalNavItem.create({href: '/c/' + category.slug + '?ascending=true&order=posts&max_posts=5', name: 'needsreply'}));
                    }
                    //there is a tag, build the url with the tagId
                    else {
                      list.push(Discourse.ExternalNavItem.create({href: '/tags/c/' + category.slug + '/' + args.tagId + '?ascending=true&order=posts&max_posts=5', name: 'needsreply'}));
                    }
                }
            } else {
                // is a sub-category
                if (excludeList.indexOf(category.slug) != -1) {
                  // in the exclude list, do nothing
                } else {
                  // if there's no tag, build url without tagId
                  if (!args.tagId) {
                    list.push(Discourse.ExternalNavItem.create({href: '/c/' + category.parentCategory.slug + '/' + category.slug + '?ascending=true&order=posts&max_posts=5', name: 'needsreply'}));
                  }
                  //there is a tag, build the url with the tagId
                  else {
                    list.push(Discourse.ExternalNavItem.create({href: '/tags/c/' + category.parentCategory.slug + '/' + category.slug + '/' + args.tagId + '?ascending=true&order=posts&max_posts=5', name: 'needsreply'}));
                  }
                }
            }

            return list;
        }
    });
</script>
