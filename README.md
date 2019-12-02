# homebrew-legacy-openssl
## これはなに
OpenSSL 1.0.x が EOL を迎えるにあたって、Homebrew の Formula からも削除されたので、tap として切り出しました。

- [homebrew-core/openssl.rb at 64555220bfbf4a25598523c2e4d3a232560eaad7 · Homebrew/homebrew-core](https://github.com/Homebrew/homebrew-core/blob/64555220bfbf4a25598523c2e4d3a232560eaad7/Formula/openssl.rb)
- [Remove OpenSSL 1.0 by fxcoudert · Pull Request #46876 · Homebrew/homebrew-core](https://github.com/Homebrew/homebrew-core/pull/46876)

## つかいかた
 ```
 % brew tap takahirohatanaka/legacy-openssl
Updating Homebrew...
==> Tapping takahirohatanaka/legacy-openssl
Cloning into '/usr/local/Homebrew/Library/Taps/takahirohatanaka/homebrew-legacy-openssl'...
remote: Enumerating objects: 4, done.
remote: Counting objects: 100% (4/4), done.
remote: Compressing objects: 100% (4/4), done.
remote: Total 4 (delta 0), reused 3 (delta 0), pack-reused 0
Unpacking objects: 100% (4/4), done.
Tapped 1 formula (30 files, 29.1KB).

% brew search openssl
==> Formulae
curl-openssl                             glib-openssl                             openssl@1.1 ✔                            takahirohatanaka/legacy-openssl/openssl  homebrew/portable-ruby/portable-openssl

% brew info takahirohatanaka/legacy-openssl/openssl
takahirohatanaka/legacy-openssl/openssl: stable 1.0.2t (bottled) [keg-only]
SSL/TLS cryptography library
https://openssl.org/
Not installed
From: https://github.com/takahirohatanaka/homebrew-legacy-openssl/blob/master/openssl.rb
==> Caveats
A CA file has been bootstrapped using certificates from the SystemRoots
keychain. To add additional certificates (e.g. the certificates added in
the System keychain), place .pem files in
  /usr/local/etc/openssl/certs
and run
  /usr/local/opt/openssl/bin/c_rehash
openssl is keg-only, which means it was not symlinked into /usr/local,
because Apple has deprecated use of OpenSSL in favor of its own TLS and crypto libraries.
```
