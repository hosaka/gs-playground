# Readme

1. When using Squash and Merge GitHub cannot sign a squash commit with our GPG key, since it does not have the private key, makes sense.
2. It does however sign it with some other key (created by default for @users.noreply.github.com perhaps?), these commits appear as unverified in the local `git log --show-signature` though unless we add the public part of this key (where do I get this?).
3. Using Rebase and Merge instead will preserve the original commit signatures but the committer needs to clean up and/or squash commits before merging.
4. Also we can use CLI to perform the Squash and Merge where we can pass the `--gpg-sign` resulting in a commit with a verified GPG signature.
