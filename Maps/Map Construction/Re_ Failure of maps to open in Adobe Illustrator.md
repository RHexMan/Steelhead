From: "NGP NGTOC TNM Help, GS-N-HQ" <tnm_help@usgs.gov>
Subject: Re: Failure of maps to open in Adobe Illustrator
Date: April 5, 2017 at 7:15:27 AM PDT
To: Rich Miller <rich@ski.org>
Cc: Laurence Moore <lmoore@usgs.gov>

Hi Rich,

This problem is touched on in the US Topo users guide (https://nationalmap.gov/ustopo/quickstart.pdf, pp. 13-14), though probably not to the depth you need. We have looked into this problem, to the extent we are able, and have basically come up empty. We are at a loss to explain why these PDFs will open most of the time in most Adobe software, and all the time in some Adobe software, but occasionally not in some other Adobe software. A plausible hypothesis is that our georeferencing process, which touches the files with non-Adobe software, is messing something up. However, we have been unable to identify any patterns that point to the actual problem or any solution. Most non-Adobe software we have tested seems to have weak layer implementations (Global Mapper and Geospatial Data Abstraction Library (GDAL) software, at least, excepted), and just can't handle the size and complexity, but you would expect Adobe software to be different. Several years ago we reached out to Adobe for help, but they apparently have no interest in the small geospatial market and basically declined to get involved. 

The overall incidence of the problem seems to be rather low, with only a few dozen reports over the last six years, though this could just mean that very few people are trying to use these files with Illustrator or Photoshop. We don't use much graphics art software, and we are not actual experts on PDF, so it is unlikely we will find or fix this bug. Hopefully it will disappear "naturally" as the software involved matures and becomes more stable.

My normal recommended work-around is to derive simpler files, such as high-res TIFFs, using Acrobat, Global Mapper, or GDAL. However, it sounds like you are doing something sophisticated enough that this may not be satisfactory. I'm afraid we did not foresee such uses for this product...the idea behind US Topo was to package GIS data in familiar map form provide simple GIS functionality to non-specialist users. We expected that advanced users would have little use for this product, but would instead use the source GIS data. 

Sorry I can't be of more help. If you find anything that points to the root of the problem, we would definitely be interested in knowing about it.

Larry

------------------------------------
Laurence R (Larry) Moore
US Geological Survey
lmoore@usgs.gov
303-202-4019

 

On Mon, Apr 3, 2017 at 7:40 PM, Rich Miller ‪<rich@ski.org>‬ wrote:
Hi,

I was referred to you by help at the USGS Store.  I am engaged in a project to make fishing maps for the California North Coast rivers.

I have been downloading your PDF 7.5 quad maps (2012 and 2015 series) from

https://store.usgs.gov/b2c_usgs/usgs/maplocator/(ctype=areaDetails&xcm=r3standardpitrex_prd&carea=%24ROOT&layout=6_1_61_48&uiarea=2)/.do

and have sucessfully edited several (removing objects, rearranging others, etc) in Adobe Illustrator (CC 2017) on a new MAC running El Capitan.  However, two unzipped files, Redcrest CA (from gda_7982168.zip) and Petrolia CA (from gda_7981896.zip)  have repeatedly failed to open.  Indeed, the attempt to open locks up Illustrator, requiring a forced quit.  I have tried many, many times, both with the 2015 and the 2012 downloads. The Redcrest 1969 map open fine, but is not in the hierarchical object format that I need.  I suspect there is some sort of PDF formatting error in these two files, and presumably in other files I have not tried.  For comparison, both Bridgeville CA and Hydesville CA 7.5’s work fine.

The question is delicate, since the Redcrest and Petrolia files open in Preview, Adobe Acrobat Reader DC, and PDFpen.  Reader even shows and manipulates the layers correctly.  On the other hand, several other PDF editors (OpenOffice (Draw), LibreOffice, Adobe Illustrator CS3) all succeed with Bridgeville and Hydesville, but fail with Redcrest and Petrolia.

Your object formatting of the national maps is really wonderful, and opens a tremendous range of possibilities for manipulation.  But, for better or worse, Adobe Illustrator is the only readily available program that has a user interface with an effective object hierarchy navigator, something that is critical is working with these very complex files.  I am hoping that there may be some sort of adjustment you can make in your map construction that would ensure that they all open in AI.

If not, or in the mean time, perhaps you can suggest some work around.  For example, I have been able to edit the maps in PDFpen to delete all the raster images, which I don’t need, and which make the files so much bigger, but these adjusted files still would not open in AI.

Best,
Rich Miller

-- 
The National Map Service Desk
United States Geological Survey
Email: tnm_help@usgs.gov
Twitter: @USGS
