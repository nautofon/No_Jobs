## No Jobs mod template for ATS

No Jobs is a template for
[American Truck Simulator](https://americantrucksimulator.com/)
mods that disable the game economy by city.


### How to create a mod using this template

You will need a text editor, such as
[BBEdit](https://www.barebones.com/products/bbedit/) /
[gedit](https://gedit-technology.github.io/apps/gedit/) /
[Notepad++](https://notepad-plus-plus.org/).

First, clone the repository or
[download the ZIP file](https://github.com/nautofon/No_Jobs/archive/refs/heads/main.zip).
You'll end up with a number of directories with ready-made mod examples
and a `template` directory.

Duplicate and/or rename the template directory to something unique for your
mod. This is now your mod's directory. In the `def` sub-directory inside it,
you will find a number of ATS data files, one for each state. The data file
for the California base map is named `city.sii`.

One by one, open these files in your text editor of choice. Each will include
a list of cities. By default, all cities are disabled. The pound/number sign
`#` at the beginning of a line is what disables a city. Remove it for those
cities that you want to enable.

For example, if you wanted to enable the cities Guymon and Tulsa, but keep
all other Oklahoma cities disabled, the file `city.dlc_ok.sii` would have to
look like this:

	SiiNunit
	{
	
	# @include "city/ardmore.sui"
	# @include "city/clinton.sui"
	# @include "city/enid.sui"
	@include "city/guymon.sui"
	# @include "city/idabel.sui"
	# @include "city/lawton.sui"
	# @include "city/mcalester.sui"
	# @include "city/oklahoma_city.sui"
	@include "city/tulsa.sui"
	# @include "city/woodward.sui"
	
	}

Do this for all the city sii files until you end up with the desired
selection of enabled/disabled cities.

Finally, edit the `manifest.sii` file. Put in something unique as display
name for your mod and your nick as the author name. Optionally, add a mod
description in a `README.txt` file or a thumbnail.

To install your mod, simply move or copy your mod's directory to the
ATS `mod` directory. It's not necessary to create a ZIP or SCS file.
The location where you can find the `mod` directory depends upon your
operating system:

*	**Linux:**  
	`~/.local/share/American Truck Simulator/mod`

*	**macOS:**  (use  **Go to Folder... ⇧⌘G**  in the Finder)  
	`~/Library/Application Support/American Truck Simulator/mod`

*	**Windows:**  
	`My Documents\American Truck Simulator\mod`

This project is placed into the [Public Domain](LICENSE).
If you share your mod with others, attribution would be appreciated,
but it's not required. Feel free to link to
the forum thread or
the [GitHub repository](https://github.com/nautofon/No_Jobs).


### No Jobs example mods

This is by no means intended to be a definitive answer to the categorization
questions posed here (for example, which are the biggest cities). It's only
meant to provide a few example scenarios for using the No Jobs template,
and perhaps a fun way to play. Even so, if you take issue with a particular
city being included or not included in these examples, feel free to comment
in the forum discussion
and I'll consider changing the city selection in a future update.

The following example mods are available:


#### No Jobs: only biggest

The "only biggest" example enables only a handful of the biggest cities.
In some cases where a big metropolitan area is split across multiple ATS
cities, close neighbors are enabled as well even though they might not
be particularly big on their own. Using this example mod will give you
a lot of opportunities to stick to freeways.

<div>
<img src="https://raw.githubusercontent.com/nautofon/No_Jobs/main/screenshots/only_biggest.png" width="280" height="280" align="top" alt="Overview map" />
<img src="https://raw.githubusercontent.com/nautofon/No_Jobs/main/No_Jobs_only_biggest/only_biggest.jpg" width="138" height="81" align="top" alt="only biggest" />
</div>


#### No Jobs: only edges

The "only edges" example enables only cities located along the edges of
the accessible world map. Looks weird, but it can help you explore some
roads that are otherwise unlikely to appear in randomly generated jobs.

For example, three roads leave Bellingham, WA: I-5 SB, SR-20 EB, SR-20 WB.
Yet, if you generate a job from Bellingham to any random city, the chance
of that route using I-5 is about 98%. The other two roads, SR-20 WB/EB,
are *almost only* relevant for jobs to Colville, Omak, and Port Angeles.
This effect can make it difficult to explore roads along the edge of the
world map during regular gameplay.

<div>
<img src="https://raw.githubusercontent.com/nautofon/No_Jobs/main/screenshots/only_edges.png" width="280" height="280" align="top" alt="Overview map" />
<img src="https://raw.githubusercontent.com/nautofon/No_Jobs/main/No_Jobs_only_edges/only_edges.jpg" width="138" height="81" align="top" alt="only edges" />
</div>


#### No Jobs: only remotes

The "only remotes" example enables only a handful of particularly
remote cities. Using this example mod will force you to drive some
rural highways. Note that "remote" doesn't mean the same thing
in Texas as it does in Idaho.

<div>
<img src="https://raw.githubusercontent.com/nautofon/No_Jobs/main/screenshots/only_remotes.png" width="280" height="280" align="top" alt="Overview map" />
<img src="https://raw.githubusercontent.com/nautofon/No_Jobs/main/No_Jobs_only_remotes/only_remotes.jpg" width="138" height="81" align="top" alt="only remotes" />
</div>


#### No Jobs: unreworked

The "unreworked" example disables those cities that are part of the
old base map (California / Nevada) and that have not yet received any
major rework since the rescale. Using this example mod may help you
to avoid areas of low graphical quality.

<div>
<img src="https://raw.githubusercontent.com/nautofon/No_Jobs/main/screenshots/unreworked.png" width="280" height="280" align="top" alt="Overview map" />
<img src="https://raw.githubusercontent.com/nautofon/No_Jobs/main/No_Jobs_unreworked/unreworked.jpg" width="138" height="81" align="top" alt="unreworked" />
</div>


#### No Jobs: one entire state

A number of examples are provided that disable all cities in exactly one
entire state. If you like, you can combine multiple of these to disable
entire regions.

<div>
<img src="https://raw.githubusercontent.com/nautofon/No_Jobs/main/No_Jobs_AZ/AZ.jpg" width="138" height="81" alt="Arizona" />
<img src="https://raw.githubusercontent.com/nautofon/No_Jobs/main/No_Jobs_CA/CA.jpg" width="138" height="81" alt="California" />
<img src="https://raw.githubusercontent.com/nautofon/No_Jobs/main/No_Jobs_CO/CO.jpg" width="138" height="81" alt="Colorado" />
<img src="https://raw.githubusercontent.com/nautofon/No_Jobs/main/No_Jobs_ID/ID.jpg" width="138" height="81" alt="Idaho" />
<img src="https://raw.githubusercontent.com/nautofon/No_Jobs/main/No_Jobs_KS/KS.jpg" width="138" height="81" alt="Kansas" />
<img src="https://raw.githubusercontent.com/nautofon/No_Jobs/main/No_Jobs_MT/MT.jpg" width="138" height="81" alt="Montana" />
<img src="https://raw.githubusercontent.com/nautofon/No_Jobs/main/No_Jobs_NV/NV.jpg" width="138" height="81" alt="Nevada" />
<img src="https://raw.githubusercontent.com/nautofon/No_Jobs/main/No_Jobs_NM/NM.jpg" width="138" height="81" alt="New Mexico" />
<img src="https://raw.githubusercontent.com/nautofon/No_Jobs/main/No_Jobs_OK/OK.jpg" width="138" height="81" alt="Oklahoma" />
<img src="https://raw.githubusercontent.com/nautofon/No_Jobs/main/No_Jobs_OR/OR.jpg" width="138" height="81" alt="Oregon" />
<img src="https://raw.githubusercontent.com/nautofon/No_Jobs/main/No_Jobs_TX/TX.jpg" width="138" height="81" alt="Texas" />
<img src="https://raw.githubusercontent.com/nautofon/No_Jobs/main/No_Jobs_UT/UT.jpg" width="138" height="81" alt="Utah" />
<img src="https://raw.githubusercontent.com/nautofon/No_Jobs/main/No_Jobs_WA/WA.jpg" width="138" height="81" alt="Washington" />
<img src="https://raw.githubusercontent.com/nautofon/No_Jobs/main/No_Jobs_WY/WY.jpg" width="138" height="81" alt="Wyoming" />
</div>
