# fakturatex

Yeah, I feel your pain – there are too many invoicing tools for Czech freelancers. Too many to choose from!

And they're all so complicated. Who needs all that stuff?<br />
You just want to fill in your details and smash that print-to-PDF button, am I right or am I right?

Sounds like you need a word template, not an app – but don't worry, you can avoid *that* torment. I present to you a brand-new invoicing tool that meets the highest standards of simplicity while respecting the ancient software engineering heritage. Standing on the shoulders of giants, leveraging tried-and-true '70s technology – you get the picture.

It's fast. Local-first. Secure. Feature-poor. Badbox-rich. ~~Written in Rust~~. *Scalable, maybe? idk. It's good.*

ℹ️ Doesn't support DPH (VAT). Or anything.<br />
It's just a plain invoice. [See example](./DEMO.pdf) 👀

## Setup locally

fakturatex runs on `pdflatex` → need to install a LaTeX distribution providing it.<br />
I recommend:
- 🪟 Windows: [MikTex](https://miktex.org/).
- 🐧 Linux: `sudo apt install texlive` _(or equivalent if not apt-based)_.
- 🍎 macOS: probably `brew install --cask mactex` via Homebrew, though I have not tested.

## Using locally

Edit `MY_DATA_GOES_HERE.tex` to fill out your personal information and toggle between fiat/bitcoin invoice.

Replace your own `signature.png` image, or disable it in the data file.

Run:

```bash
pdflatex faktura.tex
```

→ Creates `faktura.pdf` in a fraction of second ⚡🚀

## Using cloudly 🌧️

Would you like to surrender your business financial data to Github?
Or just want to play with the thing? <br />
Run [the CI action](./.github/workflows/compile.yml) to use someone else's computer.
