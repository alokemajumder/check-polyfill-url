# Polyfill URL Replacement Action

This is a GitHub Action to check for and replace `polyfill-io` URLs in the project files. Due to a recent supply chain attack affecting `polyfill-io`, this action ensures that all instances of the `polyfill-io` URL are replaced with safer alternatives provided by CDNJS.

## Details

- **Minified Replacement:** `https://cdnjs.cloudflare.com/polyfill/v3/polyfill.min.js`

This change aims to mitigate potential security risks by switching to a trusted CDN provider.

### Why This Change?

On June 2024, a significant supply chain attack was reported affecting websites using `polyfill-io`. This attack has raised security concerns and highlighted the need for immediate mitigation steps. You can read more about the attack [here](https://thehackernews.com/2024/06/over-110000-websites-affected-by.html).

### How It Works

1. The action triggers on pushes and pull requests to the main branch.
2. It checks out the repository and sets up Node.js.
3. It installs the necessary dependencies.
4. It searches for any occurrences of `https://polyfill(dot)io/v3/polyfill.min.js` and replaces them with the CDNJS equivalent.
5. It commits and pushes the changes back to the repository.

By implementing this action, I aim to enhance the security of any project by avoiding the compromised `polyfill-io` service.

---

For any issues or further information, please refer to the original article on the supply chain attack or contact the repository maintainers.

