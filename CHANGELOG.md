## 3.3.0 - 2018-05-25
**Heads up:** This update includes changes to the SEO `meta.twig`. If you are using a custom version you can review the changes [here](https://github.com/ethercreative/seo/commits/v3/src/templates/_seo/meta.twig).

### Fixed
- Fixed field settings throwing deprecation warning #109
- Fixed invalid sitemap urls
- Robot lightswitches now have a min-width #103
- Fixed TypeError in SEO variable when social image doesn't have a transform URL #101
- Fixed SEO hook throwing an error when a populated SEO field was removed from the current element #99

### Changed
- Redirect list moved below "Add Redirect" fields #107
- Empty / suffix only title fields will now populate with the element title

## 3.2.8 - 2018-05-16
### Fixed
- Fixed bug where `robots.txt` would not be accessible when not logged in. 

## 3.2.7 - 2018-05-10
**Heads up:** This update includes changes to the SEO `meta.twig`. If you are using a custom version you can review the changes [here](https://github.com/ethercreative/seo/commits/v3/src/templates/_seo/meta.twig).

### Fixed
- Fixed SEO field erroring after upgrade from Craft 2 #92
- Fixed sitemap erroring when entry doesn't have an SEO field #96

### Changed
- `og:site_name` now uses `seo.title` instead of `siteName` #95 (via @urbantrout)
- Canonical meta tag now uses `absoluteUrl` #94 (via @matthiaswh)
- Social URLs in `meta.twig` now use `absoluteUrl`

## 3.2.6 - 2018-05-01
### Fixed
- Fixed user permissions not being checked correctly #93

## 3.2.5 - 2018-04-26
### Fixed
- Fixed broken `robots.txt` code editor. #90
- Fixed sitemaps having wrong Content-Type header. #91

## 3.2.4 - 2018-04-16
### Added
- Added a "Use suffix as prefix" option to the SEO field settings. For *those* clients.

### Fixed
- The sitemap settings now show all sections, regardless of what sites they are enabled on.

## 3.2.3 - 2018-04-05
### Fixed
- Fixed bug where Craft would 500 error when robots were injected for an element without an expiry date (via @saylateam)
- Fixed a bug where the Craft edition referenced no longer existed [#81](https://github.com/ethercreative/seo/issues/81) (via @andris-sevcenko)

## 3.2.2 - 2018-03-16
### Fixed
- Fixed a bug where editing entries with an SEO field would error if the current site doesn't have a base URL. 

## 3.2.1 - 2018-03-15
### Fixed
- Fixed a bug that would cause Element API to error when no robots have been set.

## 3.2.0 - 2018-03-13
### Added
- You can now manage your sites 🤖 on a site-wide or per-field basis
	- The `X-Robots-Tag` header is added if you've set any robots
	- If the current entry has an expiry date, the `unavailable_after` directive will be added automatically
	- The `none` and `noimageindex` directives are automatically added to all pages when in `devMode`. No more accidental indexing of development sites!
- You can now manage your `robots.txt` file from the SEO settings!
	
### Changed
- Improved the settings page (now with 300% more tabs).

### Fixed
- Fixed sitemap dynamic urls throwing errors
- Sitemaps no longer show "headers already sent" warnings 
- Fixed the keywords checklist not realising content had changed on the page
- The keywords checklist now knows what spaces are and count words accordingly
- Fixed keywords checklist not working after live preview is opened
- Fixed bug where fallback social images would cause SEO field to error
- Keyword density now works correctly for keywords containing more than one word
- Fixed a bug where deleting a keyword would occasionally cause a JS error 

## 3.1.0 - 2018-03-02
### Added
- Added option to hide the social tab in the SEO field

### Changed
- It's now possible to pass social media meta to `craft.seo.custom`

### Fixed
- Fixed first paragraph check returning both positive and negative
- Snippet description now has minimum height

## 3.0.1 - 2018-01-23
### Fixed
- Fixed error when installing on Craft Personal

## 3.0.0 - 2018-01-23
### Changed
- Initial Craft 3 Release
