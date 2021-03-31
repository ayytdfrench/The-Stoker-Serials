    <head>, <body>, <p>

Start each chapter with a `head` that contains introductions to each version (if applicable). Follow `head` with `p` tags that hold each line of information (chapter, diary name, etc.)

Encode by paragraph structure set in the novel, so within `body` after `head`, begin each new paragraph with a `p` and fill the content of that tag with the text of the paragraph from the novel version.

Note: `p` tags have an indent of 4em in the stylesheet, so the first line of each new `p` tag will be indented. See <space> below for cases that need special spacing.

    <app>, <rdg>

Whenever a part of the text deviates from the novel version, nest an `app` tag followed by an `rdg` tag, all within the `p`. For the `rdg` tag, specify the version(s) by doing `rdg wit=”#version_id”` and type in the deviation before the `/rdg` end tag. Multiple `rdg` tags can be placed within the `app`. Make sure that all versions are included in an `rdg` tag whenever doing this, so that the different versions can be traced in that moment of the text. For example:

    <p>
         This is an example of how multiple versions can display
         <app>
              <rdg wit=”#version1”>Hello World!</rdg>
              <rdg wit=”#version2 #version3”>Hello, world!</rdg>
         <app>And that is that.
    </p>

Version 1 output:

  This is an example of how multiple versions can display Hello World! And that is that.

Versions 2 & 3 output:

  This is an example of how multiple versions can display Hello, world! And that is that.

In the above example, since the portion of text is wrapped within an <app> tag, that section of text will highlight simultaneously in all of the versions when a user hovers over a portion of that text in one of the versions.

    <del>

For parts of text that have been removed in a version, wrap that removed text in a `del` tag.

    <add>

For parts of the text that have been added in a version, wrap that added text in an `add` tag.

    <sic>

For parts of the text that are misspelled or appear to be typos, wrap in a `sic` tag.

    <emph>

For parts of the text that are in italics, use the `emph` tag.

    <hi>

For parts of the text with significant differences, use the `hi` tag (will have to elaborate on this and have more examples of use).

    <lb/>

Use `lb/` to mark any line breaks in the text, such as with the info that precedes each chapter or parts of the text that have different paragraph breaks.

    <space quantity=”16” unit=”char”/>

Use the `space` tag (as it is written above) for parts of the text that require an indent or that need to be in line with the start of a `p` paragraph.

    <pb/>

Use `pb/` to indicate page breaks in front matter and for versions that have multiple installments per chapter.
