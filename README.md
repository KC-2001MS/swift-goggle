# Swift Goggle

Brave Search Goggle to make it easier to get information about the Swift language.

## Description

Using this Goggle, you can re-rank Brave Search results so that information about the Swift programming language comes first.
It boosts primary sources such as swift.org, the Swift Forums and Apple Developer Documentation, along with well-known community sites, and it removes every result that does not match any of its rules.
Declarative frameworks are ranked above imperative ones, so SwiftUI appears before UIKit and AppKit.

## Requirement

Brave Search is all you need. It runs in any browser, and there is nothing to install.

<p align="center">
    <img src="https://img.shields.io/badge/Brave%20Search-Goggles-FB542B.svg" />
    <img src="https://img.shields.io/badge/License-MIT-blue.svg" />
    <a href="https://twitter.com/IroIro1234work">
        <img src="https://img.shields.io/badge/Contact-@IroIro1234work-lightgrey.svg?style=flat" alt="Twitter: @IroIro1234work" />
    </a>
</p>

## Usage

Open the link below and enter your keywords in the search box.

[Use Swift Goggle](https://search.brave.com/goggles?goggles_id=https%3A%2F%2Fraw.githubusercontent.com%2FKC-2001MS%2Fswift-goggle%2Fmain%2Fswift.goggle)

## Rules

`swift.goggle` is organised into the following sections.

| Section | What it does |
| --- | --- |
| Default action | Discards every result that no other rule matches |
| Frameworks and programming languages | Boosts SwiftUI, UIKit, AppKit, Core ML, Metal and others by keyword |
| Sites | Boosts Swift-related hosts and discards unrelated ones |
| URL paths | Boosts documentation, tutorials, forums and design pages |
| Text in URLs | Boosts Swift-related keywords on selected sites |
| Page content | Reserved for `$incontent`, currently commented out |

## Limitation

Brave Search Goggles can only match against URLs at the moment.
The `$intitle`, `$indescription` and `$incontent` targets appear in the official syntax guide, but they are documented as future work and are not implemented yet.

This Goggle therefore cannot tell whether a page is about Swift from its text.
A good article whose URL carries no Swift-related hint is discarded together with the noise.
Rules for `$incontent` are already written at the end of `swift.goggle` and are kept commented out, ready to be enabled once Brave Search ships support for them.

## Contribution

If you have a site that should be boosted or a result that should not appear, please open an [issue](https://github.com/KC-2001MS/swift-goggle/issues).

## Licence

[Swift Goggle](https://github.com/KC-2001MS/swift-goggle/blob/main/LICENSE)

## Supporting

If you would like to make a donation to this project, please click here. The money you give will be used to keep this Goggle maintained and its list of sources up to date.   
<a href="https://www.buymeacoffee.com/iroiro" target="_blank">
    <img src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" alt="Buy Me A Coffee" style="height: 60px !important;width: 217px !important;" >
</a>  
[Pay by PayPal](https://paypal.me/iroiroWork?country.x=JP&locale.x=ja_JP)

## Author

[Keisuke Chinone](https://github.com/KC-2001MS)
