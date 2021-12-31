# Deployments

There are many different types of deployments one can do, with pros and cons of each.

## Basic Deployment
In a very simple deployment all components are upgraded to a new version. It is very simple to implement, but doesn't follow any best practices on decreasing risk. If the deployment is bad you have no choice but to rollback everything.

## Multi-Service Deployment
In multi-service deployments you are doing the same kind of "all or nothing" update, however you are now  breaking down your services to their own versions. This takes away some risk (but a lot remains), and adds some complexity because you now need to consider version dependency in your testing.

## Rolling Deployment
With a rolling deployment your application is updated on a subset of nodes and then incrementally updating the remaining nodes in batches until all nodes are at the new version. This decreases the exposure of a bad release (by providing opportunities for rolling back the deployment before more users are impacted) but adds complexity by requiring you to support multiple versions at the same time while you verify each deployment step.

## Blue-Green Deployments
Blue-Green deployments have multiple environments (i.e. blue staging, green production, etc.) with each having a version of the application or service. Users are slowly migrated to the staging environment until all users have been moved to the new environment. This strategy is pretty easy to deploy because you are shifting users, not applications, and because you have 2 complete environments you can always shift all users back to the green environment. The downside is the cost and maintenance of 2 full environments.

## Canary Deployments
Canary deploymentes release an application incrementally to a subset of users in phases. It's similar to blue-green deployments in that you are controlling users shifting to the new version, but cheaper because you aren't maintaining 2 entire environments. The deployments coincide with the users being shifted. Potential negatives are testing in production and the difficulty implementing this pattern (though their are tools that can help).

## A/B Testing
A/B testing amounts to running experiments in the same environment for a period of time. "Feature flags" are commonly referred to, where either the application provider or the user can opt-in to using certain experimental features. There is potential risk in the experiments itself, and setting up the framework to run the tests.


# References
This section is summarizing this (blog post from Harness.io)[https://harness.io/blog/blue-green-canary-deployment-strategies/].
