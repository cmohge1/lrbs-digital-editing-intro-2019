---
layout: page
title:  "Day 4"
permalink: /day4/
---

<!-- @import "[TOC]" {cmd="toc" depthFrom=1 depthTo=4 orderedList=false} -->
<!-- code_chunk_output -->

* [Thursday, 27 June 2019](#thursday-27-june-2019)
	* [Summary](#summary)
	* [Aims](#aims)
	* [Outline](#outline)
		* [Principles of Annotation](#principles-of-annotation)
			* [Exercise](#exercise)
		* [Seminar 10: Genetic editing, social text editing, fluid text editing](#seminar-10-genetic-editing-social-text-editing-fluid-text-editing)
			* [Readings](#readings)
			* [Theories of textual fluidity](#theories-of-textual-fluidity)
			* [Social Text](#social-text)
			* [Genetic criticism/genetic editing](#genetic-criticismgenetic-editing)
			* [Fluid Text](#fluid-text)
		* [Seminar 11: Using TEI to encode genetic texts with TextLab](#seminar-11-using-tei-to-encode-genetic-texts-with-textlab)
			* [Exercise](#exercise-1)
		* [USTC Demo (Jessica Dalton, University of St Andrews)](#ustc-demo-jessica-dalton-university-of-st-andrews)

<!-- /code_chunk_output -->

# Thursday, 27 June 2019

## Summary

Today we will focus on recent textual scholarship on genetic criticism and social text theory, attending to questions of textual fluidity, publishing practices, and reception, in addition to considering how we build the paratextual apparatus (textual and contextual notes). We will also survey digital approaches for collating and encoding texts and doing digital book history.

## Aims

- Encode a textual apparatus, witness list, and contextual annotations.
- Understand the differences between eclectic and genetic text editing.
- Understand how text genetics and "social text" theory changed the practices of editing and a re-evaluation of authorial intention.
- A working knowledge of transcribing manuscript images.
- A facility with using digital book history tools like the Universal Short Title Catalogue.

## Outline

Time | Topic | Type |
:----|:------|:-----|
9.30 | Seminar 9: Thinking about, writing, and encoding textual apparatus and annotation | Presentation, Discussion |
11.30 | Seminar 10: Intro to genetic criticism, social text editing, fluid text editing with TextLab | Presentation  |
14.00 | Seminar 11: Continue with TextLab exercise | Digital lab |
15.30 | Digital Approaches to Book History: A USTC demo | Presentation; Digital Lab |
16.30 | Library Time |             |

### Principles of Annotation

[Click here to download the handout on annotation](../readings/on-notes.pdf)

Dr Johnson's maxim about editing: the goal is to correct what is corrupt, and clarify what is obscure.

William Empson: a great thinker about notes. See Empson's Introduction to the Notes to his *Collected Poems* (in the annotation handout). See also [Empson on annotation](../readings/empson-obscurity-and-annotation.pdf).

Remember that the essence of the app crit in TEI is the `<app>` element, which contains at least `<rdg>` elements with `@wit` attributes. If you would like to replicate Ricks's app crit, you'll want to also nest a `<lem>` element (a lemma) so that you can represent the preferred reading (the lemma) which points to its variants at the foot of the page. More information about app crit in TEI can be found in [Chapter 12](http://www.tei-c.org/release/doc/tei-p5-doc/en/html/TC.html) of the *TEI Guidelines*.

Thankfully contextual annotation is a bit simpler in TEI: for many projects a `<note>` TEI element will suffice (for more, consult the [Guidelines](http://www.tei-c.org/release/doc/tei-p5-doc/en/html/ref-note.html)).

The way you encode your annotations will depend on how you want the notes to be structured, and where you will want the notes to appear in your interface. Many projects will create a linking system for note-writing. As a simple example from the Cranch Journal project (which we examined on Day 2), the note system is constructed this way:

```
I must "see into the life of <lb/>things."<ptr target="#note9" xml:id="nr9"/>
```
Within the text I have created a `<ptr>` element with a `@target` attribute that points to the `<back>` element near the end of the file:

```
<back>
         <div type="notes">
         ... <!--skipping ahead to note 9-->

         <note xml:id="note9">"see into the life of things"] From Wordsworth's "Lines Written a
               Few Miles Above Tintern Abbey" ... </note>
```

The `<ptr>` element uses a # mark to indicate that we are going to move to another place in the file: in this case, it is to find the `@xml:id="note9"` which is properly encoded as a note in the back matter of the edition file. This essentially structures a system of footnotes (or endnotes) that link you away from the reading text.

OK, but why did the `<ptr>` element include its own `@xml:id`?

#### Exercise

(Note that you are more than welcome to attempt this exercise on a file of your own.)

1. Return to your [TEI-encoded text of Tennyson's "Early Spring"](../tennyson_early-spring.xml).
2. Create a [witness list](https://www.tei-c.org/release/doc/tei-p5-doc/en/html/ref-listWit.html) within the [<sourceDesc>](https://www.tei-c.org/release/doc/tei-p5-doc/en/html/ref-sourceDesc.html). and personography (also called prosopography) data within either `<sourceDesc>` or `<particDesc>` (within `<profileDesc>`). Create entries (and `@xml:id`s) for Alfred Lord Tennyson, Hallam Tennyson, and Christopher Ricks (it does not have to be complete).
3. Create a note to reproduce Ricks's textual headnote.
4. Create a short explanatory or textual note about some aspect of the poem in the `<back>` element (hint: a sibling of `<body>`).

If you would like to consult the Senate House Library's manuscript of "Early Spring," you can download it [here](../early-spring-ms.pdf).

### Seminar 10: Genetic editing, social text editing, fluid text editing

#### Readings

1. Jerome McGann, *Critique of Modern Textual Criticism*.
2. Hans Walter Gabler, ["The Draft Manuscript as Material Foundation for Genetic Editing and Genetic Criticism"](https://www.openbookpublishers.com/htmlreader/978-1-78374-363-6/ch10.html#_idTextAnchor027), in *Text Genetics*.
3. John Bryant, *The Fluid Text*.
4. [Hayford-Sealts genetic transcription of Melville's *Billy Budd*](https://christopherohge.com/hayford-sealts-billy-budd-transcription.pdf).

#### Theories of textual fluidity

Some distinctions:

1. New Bibliography (Greg, Bowers, Gaskell, Tanselle).
2. Sociology of Text; Social Text (McKenzie, McGann, Stillinger, Siemens).
3. Genetic editing (Zeller, Gabler, Hayford and Sealts, Bryant et al).

#### Social Text

Eclectic texts are "always dangerous" (James Thorpe, *Principles of Textual Criticism*, 190).

Limits authorial intentionality in favour of "social processes" or "bibliographic codes."

We do not own our intentions; rather they are part of the cultural structures that govern us. Intention is a sub-plot in the larger story of social interactions.

Whereas Tanselle focusses on an ontology of the intended "work," McGann uses historicist/materialist agenda to show a transaction between words and reader in certain moments. The text is more like an *event*.

**Bibliographic codes**: material and rhetorical determinants that constitute the way in which the text is presented in time.

#### Genetic criticism/genetic editing

While both are interested in determining the creative process (genesis) of a text, criticism is still deployed alongside literary theory, whereas genetic editing is a method of editing that represents the creative process using codes.

#### Fluid Text

Linguistic and bibliographic codes alone cannot always fully capture the interplay of shifting intentions, particularly in the creative process.

"In fluid text analysis, all versions are created equal" (47).

For a refresher, consult the [TEI for Transcription slides](../TEI-documentary-transcription.pdf)

### Seminar 11: Using TEI to encode genetic texts with TextLab

#### Exercise

<p>1. Go to <https://app.textlab.org/users/sign_in> and click "Sign Up." Enter your details and make sure to select "University of London" under "Institutional Sponsor."</p>

<p>2. Do you want to edit <em>Billy Budd</em> or the <em>Bow in the Cloud</em>? Find "Billy Budd (SAS, UoL)" or "Bow in the Cloud" and click "Edit."</p>

<p>3. Find your Image number on the left-hand pane and click on it.</p>

<p>4. Click on "New" on the right-hand side of the editing pane. Enter the name of your file in the following format bic_leaf[number_your initials]</p>

<p>5. Transcribe the text (all of it).</p>

<p>* setting up the leaf's structure: select the "milestone" box, and input the appropriate unit (leaf) number.</p>

<p>* link the leaf image to the transcription by clicking on the "pb" box.</p>

<p>* select the "ab" box (which will surround the text transcription).</p>

<p>* transcribe all of the <a href="https://www.tei-c.org/release/doc/tei-p5-doc/en/html/ref-metamark.html">metamark</a> elements first, then focus on transcribing the whole text.</p>

<p>6. Draw boxes around each of the revision or metamark sites. As you do so, highlight the transcribed text of the revision, then double-click on the box (near the number) of its corresponding revision site box. Enter the appropriate TEI encoding.</p>

<p>For an example of the first stanza of a poem, “The Grave of Wilberforce” (leaf 24), <a href="https://christopherohge.com/grave-of-wilberforce.xml">click here</a> (right click and download the file ("Save link as"), or click on the link, right click, and select "View Page Source").</p>

<p>7. When finished with the transcription, click "Submit."</p>

<p>8. After submission, the editor will review the leaf.</p>

<p>9. Once it is accepted and re-shared, one can then input revision narratives.</p>

<p>10. To create a revision narrative, double-click on the boxed revision site, and click "New sequence." The top level will show the zone number of the box and the bottom will allow to compose a revision narrative.</p>

For reference, [click here to download a PDF of the entire Hayford-Sealts transcription](https://christopherohge.com/hayford-sealts-billy-budd-transcription.pdf).

The ongoing digital edition can be found at the [Melville Electronic Library](http://mel-juxta-editions.herokuapp.com/documents/701).

### USTC Demo (Jessica Dalton, University of St Andrews)

The Universal Short Title Catalogue has recently released a revamped set of tools.

##### Proceed to [Day 5](day5.md)
