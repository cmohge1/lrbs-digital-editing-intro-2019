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
		* [Seminar 10: Genetic criticism, social text editing, fluid text editing](#seminar-10-genetic-criticism-social-text-editing-fluid-text-editing)
			* [Readings](#readings)
			* [Theories of textual fluidity](#theories-of-textual-fluidity)
		* [Seminar 11: Using TEI to mark-up versions of texts with TextLab](#seminar-11-using-tei-to-mark-up-versions-of-texts-with-textlab)
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

#### Principles of Annotation

[Click here to download the handout on annotation](../readings/on-notes.pdf)

Dr Johnson's maxim about editing: the goal is to correct what is corrupt, and clarify what is obscure.

William Empson: a great thinker about notes. See Empson's Introduction to the Notes to his *Collected Poems* (in the annotation handout). See also [Empson on annotation](../readings/empson-obscurity-and-annotation.pdf).

Remember that the essence of the app crit in TEI is the `<app>` element, which contains at least `<rdg>` elements with `@wit` attributes. If you would like to replicate Ricks's app crit, you'll want to also nest a `<lem>` element (a lemma) so that you can represent the preferred reading (the lemma) which points to its variants at the foot of the page. More information about app crit in TEI can be found in [Chapter 12](http://www.tei-c.org/release/doc/tei-p5-doc/en/html/TC.html) of the *TEI Guidelines*.

Thankfully annotation is a bit simpler in TEI: for many projects a `<note>` TEI element will suffice (for more, consult the [Guidelines](http://www.tei-c.org/release/doc/tei-p5-doc/en/html/ref-note.html)).

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

1. Return to your TEI-encoded text of Tennyson's "Early Spring."
2. Now have a look at [Christopher Ricks's edition](../readings/tennyson_early-spring-Ricks-edition.pdf) of Tennyson and take a moment to study the app crit of "Early Spring".
3. Within the `<text>` of your xml file, create an app crit using Ricks's example.
4. Create a personography within your file. Create entries (and `@xml:id`s) for Tennyson and Ricks (it does not have to be complete).
5. Create a note to reproduce Ricks's textual headnote (hint: treat it like you would an explanatory note: create a `<back>` element?).
6. Create a short explanatory note about some aspect of the poem.

If you would like to consult the Senate House Library's manuscript of "Early Spring," you can download it [here](../early-spring-ms.pdf).

### Seminar 10: Genetic criticism, social text editing, fluid text editing

#### Readings

1. McGann, *Critique of Modern Textual Criticism*.
2. Bryant, *The Fluid Text*.
3. [Hayford-Sealts genetic transcription of Melville's *Billy Budd*](https://christopherohge.com/hayford-sealts-billy-budd-transcription.pdf).

#### Theories of textual fluidity

Some distinctions:

1. New Bibliography (Greg, Bowers, Gaskell, Tanselle).
2. Sociology of Text; Social Text (McKenzie, McGann, Stillinger, Siemens).
3. Genetic editing (Zeller, Gabler, Hayford-Sealts, Bryant et al).

For a refresher, consult the [TEI for Transcription slides](../TEI-documentary-transcription.pdf)

### Seminar 11: Using TEI to mark-up versions of texts with TextLab

General Instructions

<p>1. Go to <https://app.textlab.org/users/sign_in> and click "Sign Up." Enter your details and make sure to select "University of London" under "Institutional Sponsor."</p>

<p>2. Do you want to edit <em>Billy Budd</em> or the <em>Bow in the Cloud</em>? Find "Billy Budd (SAS, UoL)" or "Bow in the Cloud" and click "Edit."</p>

<p>3. Find your Image number on the left-hand pane and click on it.</p>

<p>4. Click on "New" on the right-hand side of the editing pane. Enter the name of your file in the following format bic_leaf[number_your initials]</p>

<p>5. Transcribe the text (all of it).</p>

<p>* setting up the leaf's structure: select the "milestone" box, and input the appropriate unit (leaf) number.</p>

<p>* link the leaf image to the transcription by clicking on the "pb" box.</p>

<p>* select the "ab" box (which will surround the text transcription).</p>

<p>* transcribe all of the metamarks first, then focus on transcribing the whole text.</p>

<p>6. Draw boxes around each of the revision or metamark sites. As you do so, highlight the transcribed text of the revision, then double-click on the box (near the number) of its corresponding revision site box. Enter the appropriate TEI encoding.</p>

<p>For an example of the first stanza of a poem, “The Grave of Wilberforce” (leaf 24), <a href="https://christopherohge.com/grave-of-wilberforce.xml">click here</a> (right click and download the file ("Save link as"), or click on the link, right click, and select "View Page Source").</p>

<p>7. When finished with the transcription, click "Submit."</p>

<p>8. After submission, the editor will review the leaf.</p>

<p>9. Once it is accepted and re-shared, one can then input revision narratives.</p>

<p>10. To create a revision narrative, double-click on the boxed revision site, and click "New sequence." The top level will show the zone number of the box and the bottom will allow to compose a revision narrative.</p>

[Click here to download a PDF of the entire Hayford-Sealts transcription](https://christopherohge.com/hayford-sealts-billy-budd-transcription.pdf).

The ongoing digital edition can be found at the [Melville Electronic Library](http://mel-juxta-editions.herokuapp.com/documents/631).

### USTC Demo (Jessica Dalton, University of St Andrews)

The Universal Short Title Catalogue has recently released a revamped set of tools.

##### Proceed to [Day 5](day5.md)
