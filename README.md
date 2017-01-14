Run a maven project in [Concourse CI](https://concourse.ci)

First start Concourse using [Vagrant](https://www.vagrantup.com)

    $ vagrant init concourse/lite
    $ vagrant up

Then install `fly` (according to instructions in Concourse UI).

Then install the pipeline

    $ fly set-pipeline -p maven-build -c ci/pipeline.yml
