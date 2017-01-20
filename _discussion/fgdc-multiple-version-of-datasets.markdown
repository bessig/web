---
layout: default
title:  "FGDC metadata and multiple versions of datasets"
date:   2011-06-24
author: Cathy Smith
--- 
I'm looking for feedback. The NOAA climate data portal uses FGDC metadata as the only method to catalog files. We archive datasets at ESRL that are created elsewhere (and in a few cases, someone else archives a dataset created here). NOAA would like one version of FGDC metadata for each dataset. This is fine if one discusses how background of the dataset, how it was put together, areal and temporal extents and similar info. However, FGDC metadata also has info on how to read and download files. This would obviously be an issue if the data were at 2 or more places, possible in different formats as some datasets would not easily be found and the use data might be confusing. But, having multiple FGDC metadata would mean it would be hard for us to include all the correct background info (and needless to say, we would not know when it was changed at the source).

How can we reconcile the need to have one version of dataset background information yet multiple versions of how to read and get the data?

Complicating this is that we could have products created from data we archive (say, climatologies). Should we have separate FGDC metadata?

That doesn't totally make sense yet if we don't, our products are not findable. Or, we could have a subset of the whole dataset. If we point back to the originator's FGDC it might be confusing as we don't have all the variables.

Note- dataset for me refers to a collection. Say, all the NCEP/NCAR R1 products or all the CMAP precipitation products. NOT single files or variables.

We will be discussing with NCDC soon and I'd like to have a solution that leaves our products in their catalo so any feedback is helpful.

Cathy

Comments
--------

Jun 24, 2011

Anne Wilson

Hi Cathy,

I'm not sure I fully understand your situation, so I hope my comments are relevant.  Some aspects sound similar to our issues around the dynamic creation and serving of virtual datasets, subsets, aggregations, etc in a variety of output formats.  These capabilities bring up all kinds of issues around identification, provenance, and repeatability.  In fact, I presented an AGU poster last December on this subject.

The strategy we have come up with so far (not yet implemented) is to consider one version of the dataset to be the reference version from which all others can be derived.  We will maintain metadata for and curate and manage that single reference version.

We consider a subset to be a different view of the same dataset, so the same metadata applies.  Same for providing the dataset in different output formats - the same metadata applies.  An aggregation or some kind of transformation of input datasets is something new and thus would be a new dataset that would warrant it's own metadata record if it was to be persisted.

Regarding multiple locations, I suspect most metadata schemas support one or more "data access" fields, so you just add as many as you need into the metadata record.

Anne

-------------------------------

Jun 27, 2011

Cathy Smith

You do understand my question :) There are a couple of tricky aspects. We do aggregate files into longer files.

This makes access much easier for the user and at the same time we provide a different format. But, it is the same data (ignoring products).I'd rather point to their FGDC metdata for info on the dataset as they created it. I would like to be able to point them to our data access section of the metadata in their FGDC metdata so they would include ours and theirs. I think this is the ideal solution. I'm not sure how possible this isso I'll look at that more. It does tend to make it desirable that FGDC can separate out use and 'background' info.

Also, (and this is a separate issue), they are using the FGDC for data discovery. If someone finds the dataset in the noaa catalog, can they find our version as well? I think that would be very important. Right now, google finds our versions at the same 'level' as the others so presumably researchers find our versions useful. We would not want catalogs such as the noaa climate portal to reduce their visibility significantly.

