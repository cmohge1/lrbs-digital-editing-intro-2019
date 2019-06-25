---
layout: page
title:  "Day 3"
permalink: /day3/
---

<!-- TOC depthFrom:1 depthTo:6 withLinks:1 updateOnSave:1 orderedList:0-->

- [Wednesday, 26 June 2019](#wednesday-26-june-2019)
  - [Summary](#summary)
  - [Aims](#aims)
  - [Outline](#outline)
    - [Readings](#readings)
    - [Seminar 6: EEBO-TCP](#seminar-6-eebo-tcp)
    - [Seminar 7: Eclectic/copy-text/critical Editing](#seminar-7-eclecticcopy-textcritical-editing)
      - [Lecture Notes](#lecture-notes)
      - [The *apparatus criticus*](#the-apparatus-criticus)
      - [Exercise:](#exercise)
    - [Seminar 8: Open discussion of editorial problems with special collections](#seminar-8-open-discussion-of-editorial-problems-with-special-collections)

<!-- /TOC -->

# Wednesday, 26 June 2019

## Summary
Today we will cover the histories and methodologies of early modern editing and the invention of critical editions, and learn more about TEI. We will finish off the day by examining rare books and manuscripts at the Senate House Library's Special Collections.

## Aims

- An understanding of what makes an eclectic text, and how it fits into editorial tradition.
- The ability to create and encode an *apparatus criticus*.
- A set of principles for annotating scholarly editions.
- The ability to examine rare books and manuscripts and understand the challenges and decisions that go into editing them.

## Outline

Time | Topic | Type |
:----|:-----|:------|
9.30 | Seminar 6: Editing Early Modern Texts; EEBO and the Text Creation Partnership (Jonathan Blaney) | Presentation, Discussion |
11.30  | Seminar 7: Eclectic/copy text editing; Critical Apparatus | Digital lab |
14.00 (in Senate House Library Special Collections) | Seminar 8: Open discussion of editorial issues with rare books and manuscripts; mental modelling and text encoding of fiction, drama, poems––and marginalia? | Discussion; Digital lab |
16.00 | Library Time |


### Readings

1. [W. W. Greg, "The Rationale of Copy Text"](https://christopherohge.com/greg_rationale_copy-text.pdf)
2. [Fredson Bowers, "Some Principles..."](../readings/bowers_principles.pdf)
3. [Tanselle, "Varieties of Scholarly Editing".](../readings/tanselle_varieties_of_editing.pdf)
4. [Richard Bucci on Tanselle and copy-text editing.](https://christopherohge.com/bucci_on_tanselle_editing_without_copy-text.pdf)
5. Parker, *Flawed Texts and Verbal Icons*.

### Seminar 6: EEBO-TCP

Access the slides [here](LINK TBD).

* Lecture outline.
    * The history and context of EEBO-TCP
    * How the EEBO-TCP corpus was created
    * Principles and limitations
    * Some encoding peculiarities and challenges
    * Using EEBO-TCP
* The exercise
* Reading

### Seminar 7: Eclectic/copy-text/critical Editing

#### Lecture Notes

<details><summary>What is the copy-text? The Greg 'copy-text' method.</summary>
<br />
<ul>Authorial intention. The goal with so-called "copy-text" editing is to reconstruct the text that comes closest to the author's final intentions.</ul>

<ul>This comes out of two general scenarios:
<br />
1. We have an autograph manuscript and a later printing of the work.
<br />
2. We do not have a manuscript but we have multiple versions of the printed work.</ul>

<ul>In either scenario, the editor choses as "copy text" the earliest version, or (in some rare cases) some other version that appears to be closest to the author's final intentions (see Stephen Crane's <em>Red Badge of Courage</em> as an example of that rare case). Copy text is the basis of your own edited text. Some editors call it the "base text".</ul>

<ul>What did Greg actually argue?<br />

The difference between manuscript-based classical scholarship to print-based editing (i.e. when no ms survives). What the more hasty devotees of the Lachmannian method "failed to understand, or at any rate sufficiently bear in mind, was that <em>authority is never absolute, but only relative</em>" (my emphasis).</ul>

<ul>"[T]he conception of 'copy-text' does not present itself to the classical and to the English editor in quite the same way; indeed, if I am right ... the classical theory of the 'best' or 'most authoritative' manuscript, whether it be held in a reasonable or in an obviously fallacious form, has really nothing to do with the English theory of 'copy-text' at all."</ul>

<ul>It's important to stress that Greg's ideas came out of the context of Renaissance literature, which presents a textual situation that is unique from, and requires different treatment than, more recent literature (i.e., from the nineteenth and twentieth century). (See also Donald Reiman's essay in Greetham.)</ul>

<ul>Authority and essence? "[W]e need to draw a distinction between the significant, or as I shall call 'substantive', readings of the text, those namely that affect the author's meaning or the <em>essence</em> of his expression, and others, such in general as spelling, punctuation, word-division, and the like, affecting mainly its formal presentation, which may be regarded as the accidents, or as I shall call them 'accidentals', of the text."</ul>

<ul>"This distinction is not arbitrary or theoretical, but has an immediate bearing on textual scholarship."</ul>

<ul>We only select a copy-text "on grounds of expediency."</ul>
</details>

<details>
<summary><em>Substantives</em> and <em>accidentals</em></summary>
<br />
<ul>The editor is advised to select <em>substantive</em> (meaningful words) readings from the first or most authoritative printing and the <em>accidentals</em> (punctuation, spelling, capitalisation) from the manuscript or first printed source.</ul>

<ul>Individual choice in choosing among variants, including "the all-important matter of the choice of copy-text".</ul>

<ul>The tyranny of the copy-text: the failure to use individual judgment on variants and to understand the substantive and accidental differences.</ul>

<ul>E.g. Marlowe's <em>Doctor Faustus</em>. The so-called <em>B-text</em> (1616 printing) was used as copy-text in F. S. Boas's now-outdated edition. He compared this to the <em>A-text</em> (1604 printing). Consider the opening line to Faustus's opening soliloquy:<br />
<br />
<em>A-text</em>: Bid <em>Oncaymaeon</em> farewell, <em>Galen</em> come... <br />
<em>B-text</em>: Bid <em>Oeconomy</em> farewell; and <em>Galen</em> come...
<br />
<br />
The name Oncaymaeon was misprinted from copies of the A-text in 1609 and 1611, and reflected in the <em>B-text</em>. But the meter was disrupted, so the <em>B-text</em> also features a semi-colon followed by "and". Boas emended the copy-text to reflect the correct spelling of the name but kept the additions of the semi-colon and the "and" before <em>Galen</em>. What would you do? Would you keep the semi-colon? (this shows that punctuation changes are not always 'accidentals'!)</ul>

<ul>We now know that it is unwise to privilege A or B. Both texts were published after Marlowe's death, and both involved the influence of many hands other than Marlowe. During Boas's and Greg's time, the assumption was simply that the A text was corrupt because it was shorter and had mistakes. But it now appears that both the A and B texts had corruptions.</ul>

<ul>Let's divert for a moment to consider Herman Melville's <em>Moby-Dick</em>. Ahab's soliloquy in Chapter 132, "The Symphony" includes an excellent textual editing puzzle: <br />
<br />
First American edition reads, "Is Ahab, Ahab?"<br />
First English edition reads: "Is it Ahab, Ahab?"
<br />
<br />

How can you chose?</ul>

<ul>Another example from Melville: Was it right for Hershel Parker to emend Melville's line in "Hawthorne and his Mosses" to the "sacred white doe" when the published version reads: "For in this world of lies, Truth is forced to fly like a *scared white doe* in the woodlands; and only by cunning glimpses will she reveal herself, as in Shakespeare and other masters of the great Art of Telling the Truth,--even though it be covertly, and by snatches" (my emphasis). The Northwestern-Newberry critical edition of Melville's Piazza Tales and Other Prose Pieces, edited by Harrison Hayford, Alma MacDougall, and Tanselle (1987), reads "scared white doe," but a new edition of the text, based on the manuscript, was undertaken by Hershel Parker as an appendix to the Second Norton Critical Edition of Moby-Dick (2002), and the Norton Anthology of American Literature has reprinted that text instead of the NN text.</ul>

<ul>Parker justifies the thinking (albeit "edgily") behind the emendation: that the relation of Truth to the sacred is more apt to Melville's other writings, despite the fact that Melville's wife had copied out the word "scared" in the manuscript (*Herman Melville: A Biography*, vol. 1, p. 897). He also notes Melville's own comment that the published text had some errors, and presumes that the "white doe" variant was among them</ul>

<ul>Back to Greg: the circumstances of editing English texts "make it necessary to adopt in formal matters the guidance of some particular early text. If several extant texts of a work form an ancestral series, the <em>earliest</em> will naturally be selected." But this is the straightforward case. The more difficult case comes with multiple authoritative texts: "then although it will be necessary to choose one of them as copy-text, and to follow it in accidentals, this copy-text can be allowed no over-riding or even preponderant authority so far as substantive readings are concerned." The choice of readings depend on the individual judgement of the editor as to "intrinsic merit, so long as by 'merit' we mean the likelihood of their being what the author wrote rather than their appeal to the individual taste of the editor."</ul>

<ul>Sometimes the choice of copy-text "is a matter of convenience rather than of principle". Nevertheless, some principles:
<br />
<br />
1. whether the original reading can be attributed to the author;
<br />
2. whether a later reading is one that the author assented to;
<br />
3. If the answer to (1) is no, then the later reading will be right.
<br />
4. If the answer to (1) is yes, and no to (2), then the original reading should be retained;
<br />
5. If the answers to both (1) and (2) are yes, then the later reading should be adopted.
<br />
<br />
Greg's pragmatism: "The fact is that cases of revision differ so greatly in circumstances and character that it seems impossible to lay down any hard and fast rule as to when an editor should take the original edition as his copy-text and when the revised reprint."</ul>

<ul>Yet: "All that can be said is that if the original be selected, then the author's corrections must be incorporated; and that if the reprint be selected, then the original reading must be restored when that of the reprint is due to unauthorized variation."</ul>

<ul>"My desire is rather to provoke discussion than to lay down the law".</ul>
</details>

<details><summary>The Bowers method</summary>
<br />
<ul>Bowers essentially stretches the argument to the context of nineteenth century editing. He accepts the authority of the manuscript, and that the default assumption of the editor is to privilege the manuscript over the printed source (if there is no evidence the author oversaw the printing, that is). Printing simply introduces too many errors and deviates from the author's wishes.</ul>
</details>

<details><summary>A "radiating" text</summary>
<ul>Sometimes a text can only be established from copies of lost originals (more often the case with pre-Renaissance texts, but it still happens in the nineteenth century with, say, newspaper printings of lost manuscript texts).</ul>
<ul>Bucci: </ul>
</details>

Example 1: Shakespeare: [<em>King Lear</em>](../readings/greg-on-king-lear.pdf) and [<em>Othello</em>](../readings/greg-on-othello.pdf). See Greg, from *Editorial Problems in Shakespeare* and [Brian Vickers](https://www.the-tls.co.uk/articles/public/norton-new-oxford-shakespeare/).

Example 2: Milton. See [Gaskell on <em>Comus</em>](../readings/Gaskell_on_Milton.pdf); see also Empson on Bentley's editing of Milton in <em>Some Versions of Pastoral</em>.

Example 3: Dickens's <em>David Copperfield</em>. [See Gaskell on Dickens](../readings/Gaskell_on_Dickens.pdf).

Example 4: [Mark Twain's <em>Adventures of Huckleberry Finn</em>](http://www.marktwainproject.org/xtf/view?docId=works/MTDP10000.xml;chunk.id=laf858;toc.depth=1;toc.id=la0854;citations=;style=work;brand=mtp#X).

#### The *apparatus criticus*
The textual apparatus (app crit, hereafter) is one of the foundational aspects of critical editing. In eclectic text editing, it is required, because your readers need to access the variants from all of the surviving witnesses that the editor used to constructed the reading text.

Print publication: The difference between putting the app crit at the foot of the page versus in the back of the book. (Examples, from the same editor, of A. E. Houseman and Philip Larkin poems.)

For digital publication, the app crit is usually encoded within the text, though you could also use empty pointers to connect apparatus entries to the `<back>`. Most use what is called the **parallel segmentation method** for complicated, nested variants.

For more on this, consult James Cummings's [TEI for Critical Editions slides](../TEI-critical-editions.pdf).  

#### Exercise:

Access [Christopher Ricks's edition of Tennyson's "Early Spring"](../readings/tennyson_early-spring-Ricks-edition.pdf).

Encode the textual variants in the apparatus (see foot of the printed page). How can you represent those with TEI elements?

Now look at the earlier version of the poem. How could you incorporate those changes into an eclectic text of the poem?

### Seminar 8: Open discussion of editorial problems with special collections

##### Proceed to [Day 4](day4.md)
