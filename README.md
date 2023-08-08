# typst-letter
A template for creating business letters following the DIN 5008 standard.

## Overview
typst-letter provides a convenient and professional way to generate business letters
with a standardized layout. The template follows the guidelines specified in the
DIN 5008 standard, ensuring that your letters adhere to the commonly accepted business
communication practices.

The goal of typst-letter is to simplify the process of creating business letters
while maintaining a clean and professional appearance. It offers predefined sections
for the sender and recipient information, subject, date, header, footer and more.

## Example
Text source: [Musterbrief Widerspruch gegen Einkommensteuerbescheid](https://www.deutschepost.de/de/b/briefvorlagen/beschwerden.html#Einspruch)

### Preview ([PDF version](https://raw.githubusercontent.com/wiki/Sematre/typst-letter/simple_letter.pdf))
![Image of a simple letter created with typst-letter](.github/assets/simple_letter.jpg)

### Code
```typst
#import "letter.typ": letter_simple

#set text(lang: "de")

#show: letter_simple.with(
  sender: (
    name: "Anja Ahlsen",
    address: "Deutschherrenufer 28, 60528 Frankfurt",
    extra: [
      Telefon: #link("tel:+4915228817386")[+49 152 28817386]\
      E-Mail: #link("mailto:aahlsen@example.com")[aahlsen\@example.com]\
    ],
  ),
  
  annotations: [Einschreiben - Rückschein],
  recipient: [
    Finanzamt Frankfurt\
    Einkommenssteuerstelle\
    Gutleutstraße 5\
    60329 Frankfurt
  ],
  
  reference_signs: (
    ([Steuernummer], [333/24692/5775]),
  ),
  
  date: "12. November 2014",
  subject: "Einspruch gegen den ESt-Bescheid",
)

Sehr geehrte Damen und Herren,

die von mir bei den Werbekosten geltend gemachte Abschreibung für den im
vergangenen Jahr angeschafften Fotokopierer wurde von Ihnen nicht berücksichtigt.
Der Fotokopierer steht in meinem Büro und wird von mir ausschließlich zu beruflichen
Zwecken verwendet.

Ich lege deshalb Einspruch gegen den oben genannten Einkommensteuerbescheid ein
und bitte Sie, die Abschreibung anzuerkennen.

Anbei erhalten Sie eine Kopie der Rechnung des Gerätes.

Mit freundlichen Grüßen
#v(1cm)
Anja Ahlsen

#v(1fr)
*Anlagen:*
- Rechnung
```

## Usage
Download ``letter.typ`` and place ist next to your ``main.typ`` file.

## Contributing
Contributions to typst-letter are welcome! If you encounter any issues or have
suggestions for improvements, please open an issue on GitHub or submit a pull request.

Before making any significant changes, please discuss your ideas with the project
maintainers to ensure they align with the project's goals and direction.

## Acknowledgments
This project is inspired by the following projects and resources:
* [Wikipedia / DIN 5008](https://de.wikipedia.org/wiki/DIN_5008)
* [Deutsche Post / DIN 5008 Vorlage](https://www.deutschepost.de/de/b/briefvorlagen/normbrief-din-5008-vorlage.html)
* [Deutsche Post / Automationsfähige Briefsendungen](https://www.deutschepost.de/content/dam/dpag/images/P_p/printmailing/downloads/automationsfaehige-briefsendungen-2023.pdf)
* [EDV Lehrgang / DIN-5008](https://www.edv-lehrgang.de/din-5008/)
* [Ludwig Austermann / typst-din-5008-letter](https://github.com/ludwig-austermann/typst-din-5008-letter)
* [Pascal Huber / typst-letter-template](https://github.com/pascal-huber/typst-letter-template)

## License
Distributed under the **MIT License**. See ``LICENSE`` for more information.
