# Contribution Guidelines

## Introduction

Thank you for your interest in contributing to Swift Goggle, a Brave Search Goggle that re-ranks search results so that information about the Swift programming language comes first.

This project is not a Swift package. It is a single plain text file, `swift.goggle`, written in the Goggles DSL. No build step, no toolchain and no IDE are required.

## How to Contribute

Contributions to Swift Goggle are warmly welcomed and appreciated. Here are the areas where you can help:

- **Sources:** Suggest a site, a URL path or a keyword that should rank higher, or one that should not appear at all. Knowledge of good Swift resources matters far more than knowledge of the syntax.
- **Rules:** Fix rules that do not match what they were meant to match, or that catch unrelated pages.
- **Documentation:** Improve the README so that the behaviour of the Goggle is easier to understand.

## Contribution Process

### Setting Up Your Environment

1. Fork the [Swift Goggle repository](https://github.com/KC-2001MS/swift-goggle) and clone it to your local machine.
2. Open `swift.goggle` in any text editor.

### Making Changes

- Send pull requests against the `main` branch.
- Keep each rule on the line group that matches its section comment.
- Complete the Pull Request form, providing all necessary details before submitting your pull request.

### Rule Style

The syntax is described in the [Goggles quickstart guide](https://github.com/brave/goggles-quickstart/blob/main/goggles/quickstart.goggle). The points below are specific to this project.

- **Rules match against the URL only.** `$intitle`, `$indescription` and `$incontent` are documented by Brave but are not implemented yet. Rules using them are kept commented out at the end of the file.
- **`site=` matches the hostname exactly.** `site=example.com` does not cover `www.example.com` or `docs.example.com`. Add every host you mean to cover on its own line, and check where the site actually redirects to before adding it.
- **Do not use `$downrank`.** The file begins with a generic `$discard`, so anything that matches no rule is already removed. A `$downrank` rule would rescue a result from that removal and merely rank it low, which is the opposite of the intent.
- **Keep patterns distinctive.** Short substrings match far more than they appear to: `*ios*` also matches `studios` and `scenarios`, and `*ada*` also matches `metadata`. If a keyword is short or ambiguous, restrict it with `site=` instead of leaving it open.
- **Follow the existing weights.** Declarative frameworks rank above imperative ones, and official projects above unofficial ones.

  | Weight | Meaning |
  | --- | --- |
  | 8 | Declarative, official (SwiftUI) |
  | 7 | Imperative, official (UIKit, AppKit) |
  | 6 | Unofficial ports, primary sources |
  | 5 and below | Supporting material |

- **Respect the limits.** An instruction may contain at most two `*`, at most two `^`, and at most 500 characters.

### Test

- Confirm that any host you add really serves content at that exact name, redirects included.
- Before submitting a pull request, host your edited file at a URL of your own, register it at [Create a Goggle](https://search.brave.com/goggles/create) with `! public: false`, and compare a few searches with and without it.
- Check that the results you meant to bring in appear, and that nothing unrelated arrived with them.

### Submitting Your Contribution

Contributions should be made in the following manner:

1. Submit suggestions in the Issues section and ensure their acceptance.
2. Fork the repository.
3. Create a feature branch.
4. Commit your changes.
5. Push your changes to the branch.
6. Test your rules before creating a new Pull Request.
7. Create a new Pull Request.

### Code Review

Once submitted, your pull request will be reviewed. Engage with any feedback provided to ensure your contribution meets the project's standards.

### Community Standards

Swift Goggle adheres to the Contributor Covenant Code of Conduct (https://github.com/KC-2001MS/swift-goggle/blob/main/CODE_OF_CONDUCT.md) to create an inclusive and respectful environment for all users. Harassment of any kind is strictly prohibited. Kindly review the Code of Conduct for further details.

## Help

Should you have any inquiries or require assistance, please do not hesitate to contact me.

You may reach me via email at: iroiro.work1234@gmail.com

Your interest, assistance, and feedback are invaluable in improving Swift Goggle. Thank you for your continued support.

---

Keisuke Chinone  
[GitHub: KC-2001MS](https://github.com/KC-2001MS)
