# wowchemy-rtl-module
A Hugo module in order to use [Wowchemy](https://github.com/wowchemy/wowchemy-hugo-modules/) with right-to-left languages (such as Hebrew and Arabic) by converting the CSS using [RTLCSS](https://github.com/MohammadYounes/rtlcss).

## How to use
* Add to `config/_default/config.toml`:

  ```toml
  [module]
    [[module.imports]]
      path = "github.com/paazca/wowchemy-rtl-module"
  ```
* Run `hugo mod npm pack` in order to create a consolidated package.json for installing the npm dependencies.
* Additional CSS modifications for RTL languages can be added to `assets/scss/wowchemy/_rtl.scss`.
