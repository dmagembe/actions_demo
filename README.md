name: my workflow                               #workflow name


on:                                             #events that trigger this workflow
    push:
        branches: [main]

jobs:                                           #one or more jobs
    my-job:                                     #job id or job name
        runs-on: ubuntu-latest                  #runner os
        steps:
            - name: checkout code
              uses: actions/checkout@v4         #reuseable actions
            - name say hello
              run: echo "helloworld"            #shell command