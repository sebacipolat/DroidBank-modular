# DroidBank-modular

A banking app demonstrates modern Android development using Hilt, Coroutines, Jetpack Compose, Room, ViewModel, MVVM architecture.dark and ligth theme, offline support, multi module.

## Features
* Home,
* Cards
* Transactions.
* Login
* Onboarding
* Error handling

## Architecture

The following diagram sugest the way to modularizated by feature + layer


![image](https://github.com/sebacipolat/DroidBank-modular/assets/1523404/a3b72049-d307-4d5b-9419-65505f56dda0)

## TechStack:

Release process tools:

* CI/CD: [Bitrise](https://bitrise.io/)
* Repository: [Gitlab](https://about.gitlab.com/)
* Android libraries storage and distribution: [jfrog](https://jfrog.com/integration/android-repository/)
* App Distribution:  [Firebase App Distribution](https://firebase.google.com/docs/app-distribution?hl=es-419)

Quality assurance:

We will use unit test, integration test an end to end test.

* Linter: [ktlint](https://pinterest.github.io/ktlint/)
* Plugin coverage and test report_ [Jacoco: ](https://docs.gradle.org/current/userguide/jacoco_plugin.html)
* UI Test: [Maestro.dev](https://maestro.mobile.dev/)
* Unit test: Junit, mockK, Roboelectric


![image](https://github.com/sebacipolat/DroidBank-modular/assets/1523404/ded37940-5db1-42d8-9384-65e7aab67add)


Workflow:

* When some one push code to an specific branch or when a mr is trigered trough a webhook will run an specific pipeline on Bitirse.

* The pipeline will run tests and build.

* We are using jfrog Artifactory as own dependency store.

* When the final build is ready we send to Firebase app distribution to allow testers to check the app.

* The final stage will be deploy to Google Play



