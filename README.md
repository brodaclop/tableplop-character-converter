# tableplop-character-converter
Tableplop Character Export tool

Basically a bunch of type declarations that cover the `tableplop-character-v2` Tableplop character JSON file format. (`src/RawTypes.ts`)

Also contains a slightly more useful bunch of types (`src/InternalTypes.ts`) and a not-too-smart conversion from the latter to the former (`src/TPConverter.ts`)

The project can be run on the command line to produce an example JSON file that demoes the features of the conversion.

Usage: npm run run [tableplop character id] [output json file name]

The `tableplop character id` needs to be a number that belongs to a character that already exists in Tableplop, the easiest way to find this is to look at the number at the end of the character sheet URL (e.g. `https://new.tableplop.com/campaigns/654321/details/characters/123456` would have character id `123456`). Another way is to export the character and look for the number next to `characterId` in the file.

The generated file can then be imported into that character. *(There's probably no need for this warning but **PLEASE ONLY DO THIS WITH A TEST CHARACTER YOU CREATED FOR THIS PURPOSE** because `Import` overwrites the existing character.)*

As things stand, this is just a prototype, there are several things that don't work correctly or are missing entirely (the "Table" property for example), and even more that could've been done far more slicker and intuitively. But it's a start.