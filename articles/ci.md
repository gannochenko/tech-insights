# Continious integration

* [Overview](https://code-maze.com/top-8-continuous-integration-tools/)
Tools:
    * [CircleCI](https://circleci.com/)
        * cloud
        * expensive
        * 1 container for free
    * TravisCI
        * cloud, box
        * average price
        * free for opensource
    * Jenkins
        * box

* [Prettier](https://prettier.io)
* The flow schema:
    * Code
        * Typescript
        * Lint
        * Unit-tests
    * Prettier
    * Push to github
    * CircleCI / TravisCI / whatever
    * Code review
    * Pull request merge
    * Deploy to staging
    * Acceptance test
    * Deploy to production
    * Smoke test on production
