# Python_project_AWS_restart

  Problem Scenario

A learning institution named Zeta has been conducting IT training for students for over two years. One of their greatest hurdles when the training starts is setting up learner accounts and creating Linux users for their students. They have reached out and want a python script that can help them automate the whole process. Here's a breakdown of what they expect:

a) A link to an Excel file will be shared containing learners info and whose name is the 'cohort_id'
b) They want Linux users for each learner, where each learner will have an account created using their first name, have a home directory, be part of a group called 'zeta_learners', and default login password via ssh will be their first name and the first two letters in their second name e.g. if names are 'bruce wayne', their password would be 'brucewa'
c) Each day the home directories of these learners will be backed up at 4:00 AM and saved to an s3 bucket whose name is the prefix 'zeta-home-backup-' combined with the cohort_id (excel sheet name), and the name of each backup file would have the following style: dd_mm_home_backup.zip i.e. if backup runs on 28th June, the backup name would be '28_06_home_backup.zip'
Please help them with a Python script, that would parse an Excel file and retrieve the learner's details, request aws creds (access keys, and region) through a prompt, create an s3 bucket to save the backups for the learners' home directories, and create an ec2 instance which will have all the learner accounts created and have a script that runs each day to do the backups and save them on the s3 bucket.
