# Hello!

This is my website repo! I'll get round to putting some projects on it eventually :D

## Funky quirks
Because Astro builds the site elements, the actual site is in the docs folder. This is noteworthy because when you have a file called e.g. `projects.astro`, the path will be converted to `./projects/index.html`
You'll see there are lots of references to `../../thing_I_want_to_access` this is because of the quirk described above

For people forking this for their own use (or just using astro in general), to see the changes on your site you need to build it (i.e. run `npm run build`) and commit the build files (that is to say everything in the docs folder) if you're using github pages for hosting. 
