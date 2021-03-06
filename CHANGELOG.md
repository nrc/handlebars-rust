# Change Log

## [0.20.5](https://github.com/sunng87/handlebars-rust/compare/0.20.4...0.20.5) - 2016-08-27

* [Changed] Fixed issue for using [] in expression
  [#100](https://github.com/sunng87/handlebars-rust/issue/100)

## [0.20.4](https://github.com/sunng87/handlebars-rust/compare/0.20.3...0.20.4) - 2016-08-27

* [Changed] Fixed error message for partials
  [#98](https://github.com/sunng87/handlebars-rust/issue/98)
* [Added] Added support for `else` in `each` block
  [#99](https://github.com/sunng87/handlebars-rust/issue/99)

## [0.20.3](https://github.com/sunng87/handlebars-rust/compare/0.20.2...0.20.3) - 2016-08-14

* [Changed] Fixed `with` used inside `each` block [#97](https://github.com/sunng87/handlebars-rust/pull/97)

## [0.20.2](https://github.com/sunng87/handlebars-rust/compare/0.20.0...0.20.2) - 2016-08-07

* [Changed] Allowed dash character in reference
  [#94](https://github.com/sunng87/handlebars-rust/pull/94)
* [Changed] Fixed path error in nested each helpers [#95](https://github.com/sunng87/handlebars-rust/pull/95)

## [0.20.0](https://github.com/sunng87/handlebars-rust/compare/0.19.1...0.20.0) - 2016-07-31

* [Changed] Updated serde to 0.8

## [0.19.1](https://github.com/sunng87/handlebars-rust/compare/0.19.0...0.19.1) - 2016-07-26

* [Changed] Fixed `../` path visitor bug in nested `#each`
  [#93](https://github.com/sunng87/handlebars-rust/issues/93)
* [Changed] Rollback 0.19.0 change for `#if`

## [0.19.0] - 2016-07-24

* [Changed] changed `&Path` to `AsRef<Path>`
* [Changed] Fixed "../" path visitor in `#each` and `#if`.
* [Added] `set_local_path_root` and `get_local_path_root` for
  `RenderContext`.

## [0.18.2] - 2016-07-11

* [Changed] Disable `rustc_type` when `serde_type` enabled.

## [0.18.1] - 2016-07-04

* [Changed] Allow `-` char in reference.

## [0.18.0] - 2016-06-25

* [Changed] Rewrite template parser with pest.

## [0.17.0] - 2016-06-05

* [Added] JSON literals as helper param or hash, and subexpression
  return value.
* [Added] RenderError now reports template name, line and column
  number. Enabled by default. This behavior can be disabled via
  `registry.source_map_enable(false)` on production.
* [Changed] Helper API **break change**: `param(..)` and `hash(...)`
  now returns a  `ContextJson` as value which contains path as well as
  parsed Json value. No need to call `ctx.navigate(...)` any more.
* [Removed] `to_string` of `Template` and `TemplateElement` which is
  unnecessary and contains issue

## [0.16.1] - 2016-05-15

* [Removed] `num` crate dependency which is unnecessary

## [0.16.0] - 2016-03-18

* [Added] new APIs to render template string/files without
  registering to Registry
* [Added] new handlebars raw helper syntax

## [0.15.0] - 2016-03-01

* [Changed] update serde libraries to 0.7.x

## [0.14.0] - 2016-02-08

* [Added] new API: `register_template_file`
