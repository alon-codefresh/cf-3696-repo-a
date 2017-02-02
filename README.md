# Welcome

So, you've decided to try Codefresh? Welcome on board!

Using this repository we'll help you get up to speed with basic functionality such as: *compiling*, *testing* and *building Docker images*.

This project uses `[INSERT_TECHNOLOGIES]` to build an application which will eventually become a distributable Docker image.

## Looking around

In the root of this repository you'll find a file named `codefresh.yml`, this is our https://docs.codefresh.io/docs/what-is-the-codefresh-yaml[build descriptor] and it describes the different steps that comprise our process.
Let's quickly review the contents of this file:

### Compiling and testing

To compile and test our code we use Codefresh's https://docs.codefresh.io/docs/steps#section-freestyle[Freestyle step].

The Freestyle step basically let's you say "Hey, Codefresh! Here's a Docker image. Create a new container and run these commands for me, will ya?"

```
INSERT COMPILE\TEST STEP HERE
```

The `image` field states which image should be used when creating the container (Similar to Travis CI's `language` or circleci`s `machine`).

The `commands` field is how you specify all the commands that you'd like to execute

### Building

To bake our application into a Docker image we use Codefresh's https://docs.codefresh.io/docs/steps#section-build[Build step].

The Build is a simplified abstraction over the Docker build command.

```
INSERT BUILD STEP HERE
```

Use the `image_name` field to declare the name of the resulting image (don't forget to change the image owner name from `codefreshdemo` to your own!).

### Launching `[Insert this section only where applicable]`

This is where it gets real! Let's use Codefresh's https://docs.codefresh.io/docs/steps#section-launch-composition[Launch Composition step] to run our composition within Codefresh!

Launching compositions within Codefresh means you have your very own staging area, at a click of a button!
```
INSERT COMPOSITION STEP HERE
```

Using the `composition` field, we direct Codefresh to the location if the `docker-compose` file in our repository.

Once the Launch Composition step has completed successfully, you'll be able to review and share your running composition in the https://docs.codefresh.io/docs/share-environment-with-your-test[Environments page].

Now that we've gotten a grip on the flow, let's get cracking!

## Using This Example

To use this example:

. Fork this repository to your own [INSERT_SCM_SYSTEM (git, bitbucket)] account.
. Log in to Codefresh using your [INSERT_SCM_SYSTEM (git, bitbucket)] account.
. Click the `Add Service` button.
. Select the forked repository.
. Select the `I have a Codefresh.yml file` option.
. Complete the wizard.
. Rejoice!
