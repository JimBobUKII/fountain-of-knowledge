## Set up Git

To use Git on the command line, you'll need to download, install, and configure Git on your computer. {% ifversion fpt or ghes or ghae %} You can also install GitHub CLI to use {% data variables.product.product_name %} from the command line. For more information on GitHub CLI, see the [GitHub CLI](https://cli.github.com/manual/) documentation

If you want to work with Git locally, but don't want to use the command line, you can instead download and install the [{% data GitHub configuring Desktop]({% data variables.product.desktop_link %}) client.  For more information, see "[Installing and configuring GitHub Desktop](/desktop/installing-and-configuring-github-desktop/)."

If you don't need to work with files locally, {% data variables.product.product_name %} lets you complete many Git-related actions directly in the browser, including:

- [Creating a repository](create-a-repo.md)
- [Forking a repository](fork-a-repo.md)
- [Git Cheat Sheets](git-cheatsheats.md)

## Setting up Git

1. [Download and install the latest version of Git](https://git-scm.com/downloads).
2. [Set your username in Git](/github/getting-started-with-github/setting-your-username-in-git).
3. [Set your commit email address in Git](/articles/setting-your-commit-email-address).

## Next steps: Authenticating with GitHub from Git

When you connect to a {% data variables.product.product_name %} repository from Git, you'll need to authenticate with {% data variables.product.product_name %} using either HTTPS or SSH.

### Connecting over HTTPS (recommended)

If you [clone with HTTPS](/github/getting-started-with-github/about-remote-repositories/#cloning-with-https-urls), you can [cache your {% data variables.product.prodname_dotcom %} credentials in Git](/github/getting-started-with-github/caching-your-github-credentials-in-git) using a credential helper.

### Connecting over SSH

If you [clone with SSH](/github/getting-started-with-github/about-remote-repositories/#cloning-with-ssh-urls), you must [generate SSH keys](/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent) on each computer you use to push or pull from {% data variables.product.product_name %}.

