ACGI Cancer Knowledger Demo
===========================

Installation
------------

1. Install IPFS from http://ipfs.io, e.g. with a command like this:
   ```wget http://dist.ipfs.io/go-ipfs/v0.4.0/go-ipfs_v0.4.0_linux-amd64.tar.gz -O - | tar xvz; sudo mv go-ipfs/ipfs /usr/local/bin/; ipfs init```
2. Git clone this repo. You need Python installed on your machine, which is usually the case, except on Windows.

Prepare the submission
---------------------

1. Create a file with metadata that describes your VCF files. You can create a minimal one for a single VCF like this:

   ``echo '{'sample1' : {'vcf_filename' : 'test1.vcf.gz'}}' >> mySubmission.json``

   You can find a demo submission directory in ALL/.


Do the submission
-----------------
Run a command like this:
   ``submitIpfs mySubmission.json --email me@somewhere.com --institution 'University, State, Country' -name 'John Doe, MD'``

To submit the demo directory:
   ``submitIpfs ALL/ALL-US.json --email max@soe.ucsc.edu --institution 'UC Santa Cruz' -name 'Maximilian Haeussler'``

The demo data are somatic mutations from the TARGET Cancer sequencing project, ALL=Acute Lymphoblastic Leukemia.

The output looks like this:
::
    file hash: QmaV9Lme9VjjbYxaaACR7BNK5Xiae8otrRTu9Fhn3PJ7ZX
    Submission info JSON written to ALL/ALL-US.json.submitted
    Adding ALL/ALL-US.json.submitted to IPFS
    Submission ID written to ALL/ALL-US.json.submissionId
    IPFS submission OK. Submission ID is QmemBUVjsYonnibtq6Jxi8yuyxmyhEuRAZQaLbZfkv1K9X

A submission includes many files. Each file has a hash for its ID that is
unique for its content, and the overall submission has a hash for its ID that
is unique for its content, which includes the hashes of the files it contains.
Hence doing the same submission again will also give you the same submission
ID. Thus, you can always resubmit if you are not sure of the ID and
any changes to any of the files contained in the submission will result
in a different file ID and hence a different submission ID.

Note the "Submission ID". You will need it later for the block chain. 

Add the submission ID to the block chain
----------------------------------------

To do.
