# latex_util
Some LaTeX helpers...

I have developed these over time and found them useful for various papers etc. that I have been writing. I thought putting them into a repo would a) force me to clean them up a little (let's see how that goes) and b) possibly be of use to others (or not). Last, but not least, I might even learn something from one of the many LaTeX hacks out there.

There goes...

## A little bit of documentation

There are a number of `.sty` files, each of which provide helpers for handling a particular aspect of text production. These are: 

  1. `drafts.sty`, which helps with drafting by providing commands for marking up comments and identifying left-over comments when preparing the final document, as well as commands for change mark up.
  2. `figures.sty`, which provides a simplified command for embedding figures in one go
  3. `theorem_environments.sty`, which provides a number of specialised commands for theorem-style environments with a simplified usage syntax for handling labels, captions, end marks, etc.
  4. `long_paper.sty`, which provides support for separating short and long version of a paper in one TeX setup (*e.g.,* where the page limit means some information needs to go into a separate tech report).  
  5. `commands.sty` containing some miscellaneous commands probably of no use to anybody but myself :-)

### Usage of `drafts.sty`

This package provides one option `nodrafts`, so use either as `\usepackage{drafts}` or `\usepackage[nodrafts]{drafts}`. The latter will raise a warning for any comments left over in your document.

To mark up comments in the document enclose them either in `\draft{}` or `\begin{draftbar}` and `\end{draftbar}` for longer, paragraph-structured material. You can also use environment `draftlist`, which works like `draftbar` except that it turns into an enumerated list the first time you use `\item`. You do not need to explicitly open an enumeration for this to work.

For change markup there are the commands `\add{New text}`, `\delete{Old text}` and `\change{Old Text}{to new text}`. These will use color and strike-out to mark up changes in the PDF generated. If `nodrafts` has been activated, any deleted text will no longer be included and any added text will be rendered without additional colour.

### Usage of `figures.sty`

TBD

### Usage of `theorem_environment.sty`

TBD

### Usage of `long_paper.sty`

TBD
