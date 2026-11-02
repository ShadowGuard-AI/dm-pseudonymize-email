![Banner](banner.png)

# dm-pseudonymize-email
Replaces email addresses in a dataset with consistent, but fake, email addresses to preserve uniqueness without revealing actual addresses. Uses a deterministic hash based on the original email and a secret key. - Focused on Tools designed to generate or mask sensitive data with realistic-looking but meaningless values

## Install
`git clone https://github.com/ShadowGuard-AI/dm-pseudonymize-email`

## Usage
`python3 main.py EMAIL --secret_key KEY [options]`

## Parameters
- `email`: The email address to pseudonymize. Required.
- `-h`: Show help message and exit
- `--secret_key`: A secret key used to generate the pseudonym. Keep this safe! Required.
- `--domain`: The domain to use for the pseudonymized email address. Defaults to example.com.
- `--algorithm`: Hashing algorithm to use. Choices: sha256, sha512, md5. Defaults to sha256. sha256/512 are stronger, MD5 is faster.
- `--salt`: Salt to add to the email address before hashing. Improves security. Defaults to no salt.
- `--output`: Where to print the output. Choices: stdout, stderr, file. Defaults to stdout.
- `--output_file`: The file path where to store pseudonymized emails, only if output is set to file.  Defaults to pseudonymized_emails.txt.

## License
This project is released under the license in the [LICENSE](LICENSE) file. See LICENSE for details.
