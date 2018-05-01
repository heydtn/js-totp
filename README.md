[![Licence](https://img.shields.io/npm/l/express.svg)](https://github.com/heydtn/js-totp/blob/master/LICENSE)

# js-totp

A single-file purely-javascript and super basic library for generating one-time passwords (TOTP) according to [RFC 6238](http://tools.ietf.org/html/rfc6238).

This library consists of hacked and patched together implementations of TOTP and HMAC_SHA1 algorithms.  I have no promise that this is efficient, at all, though it should work for hobby purposes =).

# Description

This is a minimal lightweight library which allows generation of [Google Authenticator](https://github.com/google/google-authenticator) compatible one-time passwords.  Currently, it only supports SHA1 as the underlying digest algorithm.

# Library Usage

### OTP for current time
```javascript
totp = new jsTOTP();
totp.otp_now('supersecret'); // => "132984"
```

### OTP for custom time
```javascript
totp = new jsTOTP();
totp.generate_otp(24, 'supersecret'); // => "656025"
```

### Custom interval
By default, the interval is 30 seconds per OTP.

```javascript
totp = new jsTOTP(60);
totp.otp_now('supersecret');
```

# License

The MIT License. See [LICENSE](https://github.com/heydtn/js-totp/blob/master/LICENSE) file for details.
