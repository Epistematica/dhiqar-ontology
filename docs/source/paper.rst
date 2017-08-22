Paper «An OWL ontology for cataloguing archaeological and epigraphic finds»
===========================================================================

:Authors:
  Cristina Salonico [#]_
:Version: latest
:Date: 11th March 2013

Introduction
------------

The Dhi Qar Knowledge Base project, carried out between 2007-2008, aimed at
proposing a new way to manage archaeological and epigraphic finds by
developing a knowledge based cataloguing system.

The knowledge base was released in 2008 as the instrument for
cataloguing finds to be collected at the Nassiriya National Museum.
The work was focused especially on inscribed finds from the Dhi Qar
region (the Nassiriya district, in Iraq), such as **tablets**,
**rollers** and **envelops**, which altogether allow for an accurate
study of the **seals**. The ontology originally developed for that
knowledge base took into account characteristics of the finds
which are relevant both from an archaeological point of view (shape,
material, size and the other visual characteristics, etc.) and from
an epigraphic perspective (motives, drawings, epigraphic dating,
kind of written text, etc.). A knowledge base makes possible to ask
complex queries in order to facilitate the access to the catalogue.

This document presents the main differences between the original
ntology (published in 2008) and the new version defined in the
annexed owl file, which is a major revision of it. The revision
aims to improve the description of a few aspects of the epigraphic
domain.

It worths mention the fact that it has been designed by a **Data &
Knowledge Modeler** trained by **Epistematica** and selected among
the University of Rome Sapienza students in Philosophy.

Modifications to the original ontology
--------------------------------------

In the original ontology *BrokenEphigraphicDating* and
*NoEpigraphicDating* were disjoint classes, both included in the
super-class of all the finds missing any of the four elements that
compose a full epigraphic dating (i.e. the name of the king, the
year, month and day of his kingdom). In this way, a broken tablet
that has lost epigraphic information about dating due to accident
and a tablet on which no epigraphic information has ever been
recorded can only be distin- guished based on an active intervention
of the human agent, who has to choose
between *BrokenEpigraphicDating* and *NoEpigraphicDating* as the
specific class for classifying a given find. Moreover, it is not
taken into account the possibility that only part of the
epigraphic dating has been lost due to accident or disruption (thus
disregarding the possibility for partial epigraphic dating).

When using the present version of this ontology the expert who has
to catalogue finds must only register which dating information are
available in the set of four elements considered above. In such a
way, first of all, it is possible to register partial epigraphic
dating. Then, it is still possible also to distinguish between the
case of a find on which the epigraphic dating has been lost and the
case of an intact find on which the epigraphic dating information
has never been written. In this way, three possibilities are given:

1. The agent records the appropriate value for any of the four elements
   of epigraphic information (*epigraphicKing*, *epigraphicDay*,
   *epigraphicYear* and *epigraphicMonth*) and possibly enters the value
   ``0`` for one or more elements which may have been omitted in the
   epigraphic dating.

2. The agent records the value ``0`` for all the four element of the
   epigraphic information when the whole epigraphic dating information
   has been omitted (i.e. the find is intact and there is no dating
   information).

3. The agent records no value for any single epigraphic information
   element when the find is broken, unless one or more of them are
   present (at most three).

    In order to realize the modifications described above we have
    changed the range of the datatype property *epigraphicKing* in any
    (previously it was string) and we have added a common super-property
    *epigraphicDating* containing the four distinct properties
    *epigraphicKing*, *epigraphicYear*, *epigraphicMonth* and *epigraphicDay*.

Annex
-----

.. note:: The ontology in OWL format **DhiQar.owl**

-------------------------------

.. [#] Master degree in Philosophy

|
|
