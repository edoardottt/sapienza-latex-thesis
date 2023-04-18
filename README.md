LaTeX package for thesis cover page in compliance with Sapienza guidelines, see [here](http://www.uniroma1.it/sites/default/files/allegati/esempio%20frontespizio%20elaborato.pdf) for an example and [here](http://www.uniroma1.it/logotesi) for complete guidelines. The package is provided *as-is*, with no warranty of any kind.

The logo (`.eps` file) was obtained by converting (with Inkscape) the `.ai` file available on the website of Sapienza (see [here](http://www.uniroma1.it/sites/default/files/allegati/ml_alta_risoluzione.zip)).

## Instructions

The package modifies the `\maketitle` command to create a front page that complies with Sapienza's instructions.

The `test.tex` file provides an example of how to use the package.

### Setting up the content of the title page

To set the various fields required in the cover page, use the following commands:
- `\STTitle{title}` to set the thesis title.
  To insert a line break within the title, use `\protect\newline`.
  The command also sets the value of `\title{}`;
- `\STFaculty{faculty}` to set the faculty.
  Only specify the faculty, e.g., "Philosophy, Literature, Humanistic Studies and Oriental Studies", and not the text *Faculty of*;
- `\STBCourse{bachelor degree course}` to set the bachelor degree name.
  Only specify the degree course, e.g., "Ancient History", and not the text *Bachelor's Degree in*;
- `\STMCourse{master degree course}` to set the master degree name.
  Only specify the degree course, e.g., "Ancient History", and not the text *Master's Degree in*;
- `\STChair{chair}` (optional) to set the chair;
- `\STCandidate{student name}` to set the name of the student.
  The command also sets the value of `\author{}`;
- `\STMatricola{student ID number}` to set the student's ID number;
- `\STSupervisor{supervisor name}` to set the name of the supervisor or instructor;
- `\STCoSupervisor{co-supervisor name}` (optional) to set the name of the co-supervisor;
- `\STAcademicYear{academic year/academic year}` to set the academic year.
  Only specify the year, e.g., "2022/2023", and not the text *academic year*.

> **Note**
> Only one between STBCourse and STMCourse must be specified.

*Chair* and *Co-supervisor* may not be specified, in which case they will not appear on the title page. Every other field must be specified.

#### Note on supervisor and co-supervisor

For bachelor's degree graduates, the supervisor may be referred to as "responsible", and the co-supervisor as "co-responsible".
To modify the wording indicative of supervisor and co-supervisor, use the commands `\STTextSupervisor{text}` and `\STTextCoSupervisor{text}`.
Both fields are initially set as *Supervisor* and *Co-supervisor*.

### Title page style

The title is formatted according to the specifications provided by Sapienza:
- title, faculty, and degree course in color `RGB(111,10,25)`;
- Arial font;
- 20pt for the title, 10pt for the rest;
- bold for the faculty and degree course.

The text is left-aligned, on the *S* of the Sapienza logo.
The specified settings do not affect the rest of the document.

The margins are set (left, top, right, bottom) to 4cm, 2.75cm, 2.5cm, 1cm.
They do not affect the margins in the rest of the document.

### Setting spaces

The fields are printed in the following order:

1. Thesis title;
2. Faculty, (bachelor or master) degree course, and optionally chair;
3. Candidate and matriculation number;
4. Supervisor and optionally co-supervisor (the latter moved to the right);
5. Academic year.

It is possible to adjust the vertical space between the different fields:
- `\STSapienzaTitleSpace` sets the space between the Sapienza logo and the title;
- `\STSapienzaFacultySpace` sets the space between the title and the faculty;
- `\STSapienzaCandidateSpace` sets the space between the faculty and the candidate;
- `\STSapienzaSupervisorSpace` sets the space between the candidate and the supervisor;
- `\STSapienzaAcademicYearSpace` sets the space between the supervisor and the academic year.

The space between the fields is set with `\setlength{space name}{value}`.

---------

This is a fork of [asmeikal/FrontespizioSapienza](https://github.com/asmeikal/FrontespizioSapienza) to support English language.
