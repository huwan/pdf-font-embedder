# PDF Font Embedder

This repository contains two bash scripts, `fontcheck` and `fontembed`, that can be used to check for embedded fonts in a PDF file and to embed fonts if they are not already embedded. These scripts are particularly useful for ensuring that all fonts are embedded in your manuscript before submitting it to conferences and journals.

## Prerequisites

Before using these scripts, you need to install the following tools on your macOS system:

- `poppler` or `xpdf` for checking fonts in PDF files.
- `ghostscript` for embedding fonts in PDF files.

You can install these tools using Homebrew:

```sh
brew install poppler
brew install ghostscript
```

## Installation

1. Clone this repository to your local machine:
    ```sh
    git clone https://github.com/huwan/pdf-font-embedder.git
    cd pdf-font-embedder
    ```

2. Copy the scripts to `/usr/local/bin`:
    ```sh
    sudo cp fontcheck /usr/local/bin
    sudo cp fontembed /usr/local/bin
    ```

3. Make the scripts executable:
    ```sh
    sudo chmod +x /usr/local/bin/fontcheck
    sudo chmod +x /usr/local/bin/fontembed
    ```

## Usage

### Checking for Embedded Fonts

To check if fonts are embedded in a PDF file, use the `fontcheck` script:

```sh
fontcheck file1.pdf file2.pdf ...
```

or

```sh
fontcheck *.pdf
```

This will output the font information for each PDF file specified.

### Embedding Fonts

To embed fonts in a PDF file, use the `fontembed` script:

```sh
fontembed file1.pdf file2.pdf ...
```

or

```sh
fontembed *.pdf
```

This will embed fonts in each PDF file specified and overwrite the original file.

## Example

```sh
# Check fonts in a PDF file
fontcheck sample.pdf

# Embed fonts in a PDF file
fontembed sample.pdf
```

## Acknowledgements

Special thanks to the developers of `poppler`, `xpdf`, and `ghostscript` for their invaluable tools.
