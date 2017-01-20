---
layout: default
title:  "Human vs Machine Readable metadata issues"
date:   2011-04-21
author: Cathy Smith
--- 

Comments
--------

Apr 21, 2011

Cathy Smith

The subject of machine vs human readable metadata came up briefly at the first meeting. This is an issue in netCDF files. Time values and metdata often use udunits which is easily machine readable but not as easily human readable. And, when it is used, some natural time units such as 'months' are discouraged. NetCDF CF doesn't have output model resolution as an attribute, something that is often wanted by researchers. It is possible to get this from the file but it is not trivial. It seems that making file metadata more useful by computers can make it harder on people. Without essentially duplicating attributes in files, it is not easy to make metadata both human and machine readable and techies tend towards satisfying the latter need.

Cathy

----------------------

Apr 21, 2011

Leonard Sitongia

Can you give an example, for time?  Are you saying that a metadata element for time cannot be expressed as something like YYYY-MM-DD HH:MM:SS?

Are you looking for a format which you can look at directly at a Unix command line, for example with "more", so that you can see some of the metadata?

------------------------

Apr 21, 2011

Cathy Smith

This is more of a philisophical thing than something I can't do. UDUNITS has something like hours since a start date. When a human does a ncdump, they only see dates as something like "450012". Computers can easily figure this out, of course, but there is a a fundamental disconnect sometimes between human readable metadata and metadata meant for programs to interpret.

Cathy

--------------------------

Apr 21, 2011

Leonard Sitongia

Sure, I see what you mean.