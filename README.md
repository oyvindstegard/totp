# Implementation of TOTP in a shell script

The implementation is described in this blog post:
https://stegard.net/2023/11/implementing-a-time-based-one-time-password-totp-generator/

## Requirements

The following commands must be available in your `PATH`:

1. openssl
2. base32
3. xxd

## Usage

    $ echo "SOME_TOTP_BASE32_KEY" | ./totp

    $ ./totp < .some_file_with_base32_key
    
    $ gpg -d some_file_with_base32_key.gpg | ./totp
    
## Example

    $ echo XCGVLAD4EMLOV72B | ./topt
    532405

## Verify

Check results using https://www.verifyr.com/en/otp/check#totp
