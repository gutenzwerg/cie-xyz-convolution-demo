# cie-xyz-convolution-demo
Colour Science: Convolution instead of Confusion in CIE XYZ.

Many students initially experience colourimetry as a collection of abstract formulas, integrals and standard tables.

I therefore developed an interactive HTML/JavaScript demonstration that visualises the complete chain:

Reflectance curve → Illuminant → Stimulus curve Φ(λ) → Convolution with the CIE colour matching functions → CIE XYZ

Arbitrary reflectance curves can be drawn directly with the mouse. This makes it possible to experiment interactively with very different materials and printing inks.

There is also a “Discrete Summation Mode”, in which the spectra are displayed not as smooth curves but as individual 5 nm wavelength intervals.

The “integrals” are numerically actually sums.

Technically, the project is based on:
• real CIE 1931 2° colour matching functions
• real D50/D65 spectral distributions
• pure HTML/CSS/Vanilla JavaScript
• a central language block for German/English

Ultimately, it is simply a standalone HTML page that should run in any modern browser.

The tool was developed for vocational education in printing and media technology.

© Christian Greim
Created with support from ChatGPT / OpenAI
CC BY-SA 4.0

#ColourScience #ColorManagement #CIE #Printing #Visualization #Education #JavaScript #HTML

# Language Switching / Internationalisation

The user interface texts are stored centrally in the JavaScript object TEXT.

To switch between English and German, search for:

const UI_LANGUAGE = "en";

and change it to:

const UI_LANGUAGE = "de";

Additional languages can easily be added by extending the TEXT object with another language block.

The program logic, variable names and comments are intentionally kept in English so that AI tools and translators can generate additional language versions more reliably.

A practical workflow for creating a new language version is:

Copy one existing language block from the TEXT object.

Rename it, for example:

fr: { ... }
Translate only the visible UI texts.
Leave all JavaScript identifiers, formulas and internal structures unchanged.

Because all visible text is collected in one place, AI tools such as ChatGPT can usually translate the interface reliably without modifying the program logic.
