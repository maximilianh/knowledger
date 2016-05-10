===================================
ACGI Knowledger Demo Implementation
===================================

Installation
------------

1. Install IPFS from http://ipfs.io
2. Run "ipfs init"
3. Git clone this repo. You need Python installed on your machine, which is usually the case, except on Windows.

Prepare the submission
---------------------

1. Create a file with metadata that describes your VCF files. You can create a minimal one for a single VCF like this:

   ``echo '{'sample1' : {'vcf_filename' : 'test1.vcf.gz'}}' >> mySubmission.json``

   You can find a demo submission directory in demoSubmit/.


Do the submission
-----------------
Run a command like this:
   ``submitIpfs mySubmission.json --email me@somewhere.com --institution 'University, State, Country' -name 'John Doe, MD'``

To submit the demo directory:
   ``submitIpfs demoSubmit/ALL-US.json --email max@soe.ucsc.edu --institution 'UC Santa Cruz' -name 'Maximilian Haeussler'``

The output looks like this:
    ...
    file hash: QmaV9Lme9VjjbYxaaACR7BNK5Xiae8otrRTu9Fhn3PJ7ZX
    Submission info JSON written to demoSubmit/ALL-US.json.submitted
    Adding demoSubmit/ALL-US.json.submitted to IPFS
    Submission ID written to demoSubmit/ALL-US.json.submissionId
    IPFS submission OK. Submission ID is QmdQa1CXBKj93Y8Gyo2DSpVmSE1rrNFt8bshQ1RBFFhwGh

Note the "Submission ID". You will need it later for the block chain. If you forget it, it has also been written to a file alongside your .json file. Note that doing the same submission again will also give you the same submission ID, so you can always resubmit if you are not sure of the ID.

Add the submission ID to the block chain
----------------------------------------

To do.
