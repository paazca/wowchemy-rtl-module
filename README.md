# wowchemy-rtl-module
A Hugo module in order to use [Wowchemy](https://github.com/wowchemy/wowchemy-hugo-modules/) with right-to-left languages (such as Hebrew and Arabic) by converting the CSS using [RTLCSS](https://github.com/MohammadYounes/rtlcss).

## How to use
* Add to `config/_default/config.toml` (make sure it's imported before wowchemy):

  ```toml
  [module]
    [[module.imports]]
      path = "github.com/paazca/wowchemy-rtl-module"
  ```
* Run `hugo mod npm pack` in order to create a consolidated package.json for installing the npm dependencies.
* Additional CSS modifications for RTL languages can be added to `assets/scss/wowchemy/_rtl.scss`.


### Note:
This module was built for Wowchemy v5.0.0-beta.0. Using a different version may require you to modify `layouts/partials/site_head.html` by replacing `{{ $style := slice $css_bundle_head $style | resources.Concat "css/wowchemy.css" }}` with `{{ $style := slice $css_bundle_head $style | resources.Concat "css/wowchemy.css" | resources.PostCSS }}`
