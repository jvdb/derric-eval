## Derric DSL evaluation results repository

This repository contains the results of the [Derric](http://derric-lang.org/) DSL evaluation conducted using the Wikipedia image file corpus.

### Source data

Source for the corpus is the file `images.lst` in the root directory of this repository, containing a static listing of all image URLs on Wikipedia, dated 06-2008.
Original URL for this file was [http://static.wikipedia.org/downloads/2008-06/en/images.lst](http://static.wikipedia.org/downloads/2008-06/en/images.lst), but since it is no longer available at that location, it is mirrored in this repository.
The listing contains more files than in our evaluation, because we have filtered it to remove:

1. Smaller versions of the same file (e.g., thumbnails).
2. Files with other file extensions than JPG/JPEG, GIF, and PNG.

Additionally, when we downloaded the remaining files, only approximately 50% was still available. Each format's directory contains a file with the resulting set of files used.

### Result data

In the current state of the repository, each directory contains the final state of the evaluation: the final Derric description, the final error listings (empty in all cases, since all files could be described) and the original full input listing.

Apart from some overhead commits (such as the one adding this file to the repository), each commit represents a modification to a Derric description and contains:

1. The modified Derric description of the respective format.
2. An updated error list as a result of applying that modification.
3. A sample file in the `samples` subdirectory, illustrating the addressed issue.

