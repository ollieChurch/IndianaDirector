# Theatre Director's Portfolio Site
This is a portfolio site designed and coded to a brief for award winning theatre director Indiana Lown-Collins. You can visit the live site at [indianalowncollins.co.uk](indianalowncollins.co.uk)

## The Process
Indiana and I caught up to talk through the aims of her portfolio site and the content she wanted to showcase. Once this was complete I set about creating a rough sketch on paper of the site's UI and it's flow before putting the structure together in Vue, using Bootstrap to speed up the CSS and give a modern feel.

Once I had a prototype site, I presented this to Indiana who provided me with feedback against her expectations. Using the feedback I reworked certain design elements and fleshed out the prototype site.

Next was to incorporate a CMS so that Indiana could edit the content of her site without needing to go through me. I chose *NetlifyCMS* for this project as I had used it previously and been happy with the results. It includes *Netlify Identity* to authorise Indiana as an editor for the site.

To make full use of the Netlify eco-system, the site's contact form uses *Netlify Forms* to filter out spam and take in correspondence, alterting Indiana to new contacts via email notification.

Finally I presented Indiana with her site, hosted on Netlify, which she has updated with the relevant content. I continue to maintain the site in other respects.

## The Technology
This is a site built with Vue and Bootstrap. *NetlifyCMS* stores it's saved content as a JSON files in the GitHub repo and I make use of this file within the vue script to display the data where it is needed throughout the site. Thanks to Netlify's continuous build functionality, everytime the GitHub repo is updated Netlify triggers a new build incorporating any fresh edits Indiana has made instantly.

## Next Steps
Currently all of the main page vue code is in one file, and while it is relatively simple, it could do with refactoring and splitting out into components for reusability.
