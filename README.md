# SPSM — Simple Password Strength Meter

SPSM is a lightweight, client-side password strength meter using [zxcvbn-ts](https://zxcvbn-ts.github.io/zxcvbn/).

It provides local password strength analysis and an optional [Have I Been Pwned](https://haveibeenpwned.com/) check using the Pwned Passwords API's k-anonymity mechanism.

## Features

* Client-side password strength analysis
* Powered by zxcvbn-ts
* Strength score from 0–4
* Password feedback and estimated guesses
* Optional HIBP Pwned Passwords check
* HIBP check uses k-anonymity
* Password is never sent directly to HIBP
* No accounts
* No backend
* No database
* Single `index.html` file

## Usage

Download or clone the repository and open `index.html` in a modern web browser.

SPSM loads zxcvbn-ts and its language/matcher packages from jsDelivr, so an internet connection is required for the application to load those dependencies and perform the optional HIBP check.

## Privacy

Password strength analysis is performed locally in the browser.

The optional breach check uses HIBP's k-anonymity system. Only a partial SHA-1 hash prefix is used for the API request; the complete password is not sent to Have I Been Pwned.

The HIBP check only runs when the user explicitly requests it.

## Browser Support

SPSM requires a modern browser with support for:

* JavaScript modules
* `fetch()`
* Web Crypto APIs

Older browsers may not be supported.

## License

See the [LICENSE](https://github.com/nxs8739/spsm/blob/main/LICENSE) file for licensing information.
