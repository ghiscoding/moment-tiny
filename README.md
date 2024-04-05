[![npm version](https://badge.fury.io/js/moment-tiny.svg)](https://badge.fury.io/js/moment-tiny)

# moment-tiny

This package exposes 2 builds from the MomentJS projects (CJS and ESM), both of the files are pulled from the [GitHub/Moment](https://github.com/moment/moment/) project, so that you can use as an npm module so you can import/require the minified version of moment into your projects without the bloat of the locales.

- CJS which is [`/moment.js`](https://github.com/moment/moment/blob/develop/moment.js) (not minified) located at GitHub/Moment project root.
- ESM which is [`/min/moment.min.js`](https://github.com/moment/moment/blob/develop/min/moment.min.js) (minified) located in GitHub/Moment project `/min` folder
  - the ESM build was detailed in this MomentJS [commit](https://github.com/moment/moment/commit/87994b745c20febf378ccd8f2dc190cd8d225020).

This package will follow the [moment.js releases](https://github.com/moment/moment/releases).

### What's the difference with [`moment-mini`](https://github.com/ksloan/moment-mini)?

The difference is that `moment-mini` is only including the CJS build, however I'm more interested in the ESM build which is also included in here. I also added `exports` in the `package.json` for better support as shown on the [Are the types wrong](https://arethetypeswrong.github.io/?p=moment-tiny) website.

To be clear, MomentJS already has both CJS/ESM builds (which is where we are getting the files from), **but** with bundlers like WebPack, it often bloats the install by including all locales which we will not include in here.
