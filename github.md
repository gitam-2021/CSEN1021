# GitHub

For CSEN1021 course we rely on `git`, a popular tool for saving different versions of code, and [GitHub](https://github.com/), a popular website for saving those versions in the cloud. To push (i.e., save) your code to GitHub using `git`, you need to log in using [SSH](#ssh).

***

## SSH

1. Open a terminal window, if not open already, within [Visual Studio Code](/code/).
1. Execute `ssh-keygen`. When prompted to "save the key," just hit Enter, without typing anything.
1. You'll then be prompted for a "passphrase" (i.e., password). No need to input a passphrase; just hit Enter. You'll then see a "randomart image" that you can ignore.
1. Execute `cat ~/.ssh/id_rsa.pub`. You'll then see your "public key," multiple lines of seemingly random text. Highlight and copy all of those lines, starting with `ssh-rsa` to the end. **But don't highlight your terminal window's prompts (which contain `$`) before or after those lines.**
1. Visit [https://github.com/settings/keys](https://github.com/settings/keys), logging in with your GitHub username and password as usual. Don't use the passphrase you just created, if any.
1. Click **New SSH Key**.
1. Paste your public key into the text box under **Key**. Optionally input a title under **Title** (e.g., `CSEN1021-CS50`).
1. Click **Add SSH Key**.
1. Execute `ssh -T git@ssh.github.com -p 443`.  You should be greeted with "Hi USERNAME! You've successfully authenticated, but GitHub does not provide shell access."  If you don't see that, review the above steps to verify you didn't skip something.

You should now be able to use `check50` and `submit50` (and `git`) without GitHub username and password. But if you created a passphrase, you might still be prompted for that.

***