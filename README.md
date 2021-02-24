# opennmt-iterator
This script will run onmt_train on all .yaml and .yml files in the directory you specify.
This is so you can train multiple networks in sequence without starting the training manually. This currently only works opennmt-py

This is a work in progress. I am planning to add:

    functionality for opennmt-tf
    
    onmt_translate and onmt_build vocab
    
    iteration over all sub-folders

Step 1: Have a directory where one or more *correctly configured* .yaml files are located. The directories in the yaml files have to be configured in such a way that the execute_all script can find your corpus files, so it is safest to specify the full directory in your yaml file.

Step 2: Run execute_all.py from your command line, with the --dir DIRECTORY argument filled. The optional argument -iter allows you to iterate over all immediate subdirectories of the directory you specified with --dir.

Your opennmt-py will now train all the models for which you created .yaml files in succession.
