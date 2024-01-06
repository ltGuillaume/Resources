My releases have corresponding GPG signed `*.sha256` files. You can use [gpg (GnuPG)](https://gnupg.org) to verify that the builds haven't been tampered with by the server or while in transit.

#### First time only:
1. Download my public key [ltguillaume-signing.key](ltguillaume-signing.key)  
    The public key's fingerprint is `2D4A31E7F5DA47ECA08E9668F965AFD64E967D2A`
2. Import the key:
    ```
    gpg --import ltguillaume-signing.key
    ```

#### Verify the build:
1. Download the release's `[Program-Name_x.x.x].zip` and `[Program-Name_x.x.x].sha256` files
2. Verify the hash file and check the .zip's hash:
    ```
    gpg --verify [Program-Name_x.x.x].sha256
    sha256sum -c [Program-Name_x.x.x].sha256
    ```