# kingsquare/mongodb-via-automation

A simple mongodb initialized via the MMS automation agent

# Running

     docker run -d \
         -p 27017:27017 \
         kingsquare/mongodb-via-automation:1.5.3 \
         --mmsBaseUrl=https://mms.mongodb.com \
         --mmsGroupId=<YOUR MMS GROUP ID> \
         --mmsApiKey=<YOUR MMS API KEY> \

# Running with config files

This is another possibilty. The contents of the two variables should be moved to a seperate config file with the following contents:

    mmsGroupId=<YOUR MMS GROUP ID>
    mmsApiKey=<YOUR MMS API KEY>

Afterwards just run the container as;

     docker run -d \
         -p 27017:27017 \
         -v your-config-file:/etc/mongodb-mms/automation-agent.config
         kingsquare/mongodb-via-automation:1.5.3

# Future updates

I'll try to keep the agent and docker releases in check by utilizing the same agent version as docker image tag