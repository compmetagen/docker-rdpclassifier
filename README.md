# RDP classifier - Docker

[Ribosomal Database Project (RDP)](https://sourceforge.net/projects/rdp-classifier/files/rdp-classifier/) Classifier in a Docker image.

RDP provides quality-controlled, aligned and annotated Bacterial and Archaeal 16S rRNA sequences, and Fungal 28S rRNA sequences, and a suite of analysis tools to the scientific community.

## Available Tags/Versions

- latest: GitHub snapshot (master)
- 2.12: RDP Classifier Release 2.12
- 2.11: RDP Classifier Release 2.11

## Quickstart

1. Download the latest version:

   `docker pull compmetagen/rdpclassifier`

2. Run an instance of the image, mounting the host directory:

   `docker run -t -i -v /Users/davide/rdp:/rdp -w /rdp compmetagen/rdpclassifier /bin/bash`

3. Check the RDP Classifier version:

   `root@44b2c8de4e4e:/rdp# echo $RDP_VERSION`

4. Run the RDP Classifier:

  `root@44b2c8de4e4e:/rdp# java -Xmx2g -jar $RDPPATH/dist/classifier.jar classify input.fna -o output.txt`
