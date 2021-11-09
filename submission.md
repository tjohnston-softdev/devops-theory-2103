# DevOps Theory

---

### Why is it important to add branch policies to prevent direct commits to the 'main' branch?

It is important to have policies on the main branch in a Git repository in order to ensure proper versioning. The idea with branching is that 'main' refers to the stable, public version of the software. When developers want to work on new features for a future version, they can develop as normal but commit their changes to separate branches. That way, the revised code branches off the stable 'main' commit without affecting or breaking it.

For example, when somebody views an open-source project, they would most likely want the most recent stable release. Therefore, they will clone the repository from the 'main' branch. If for some reason they feel like contributing, they can commit changes into their own branch and proceed safely. If they end up breaking something, those issues remain isolated in the separate branch.

Once the contributor is happy with their changes to the software or a developer thinks their version is ready, they can submit a 'pull request'. When you do this, it basically says to the administrator: "Here are some changes I want to make". The administrator can then review those changes. If they are satisfied, the updated branch can be merged back into 'main'. By default, the commits will be added onto the main branch and a new version of the software is created.

As for the branch policies in Azure, the exact implementation would depend on the project. For the purposes of this assessment, I enabled 'Require a minimum number of reviewers' with the amount set to 1, and the most recent pusher is prohibited from approving their own changes. That way, I cannot make direct commits to the 'main' branch. Instead, I must make a pull request which will be reviewed by a superior, presumably [the hiring manager].

To demonstrate, I tried making a commit to the 'main' branch [with changed files]. Because of the branch policies, I got an error. However, when I made my own branch 'tjohnston-dev', I was allowed to commit as normal. That way, I can do what I want on my own branch and cannot merge into 'main' without making a pull request.

---

### Explain Continuous Integration in a software project.

Continuous Integration is the automated process of integrating code changes from multiple contributions within a software project. In other words, developers can merge their code changes into a central repository which can then be built and tested.

Before CI, developers had to manually coordinate and communicate their respective contributions to the overall project. The resulting communication overhead caused a longer amount of time between releases, and a higher rate of failure. This was due to the energy developers spent trying to avoid their integrations conflicting with each other, or perhaps even breaking the previous stable version entirely. These problems did not just affect the development team. It also hampered communication between different teams such as product management. For example, a product manager might request a new feature, but it became hard for the developers to estimate when it would be implemented due to the aforementioned risk of failure.

CI improves the productivity and output of development teams by allowing individuals to work on their respective tasks concurrently rather than one-by-one. Once their work is complete, the contributions are integrated into the final result independently and rapidly. CI is generally used as part of an agile workflow with tasks distributed among members as needed.

One benefit of CI is that the development team and their code base can scale with as little communication overhead as possible. Developers can work on their own tasks in isolation without any organizational dependencies between features, and the assurance that their code will seamlessly integrate with the code base as a whole.

Another benefit of CI is faster feedback regarding business decisions. Product teams are able to test ideas and iterate designs faster. Changes can be rapidly integrated and tested accordingly. If there are any bugs as a result of the changes, they can be addressed and fixed quickly. If there is a fatal issue with the new code, the changes can be rolled back.

A final benefit of CI is improved communication. This includes transparency and insight into the process of software development, as well as greater collaboration between development and operations (Hence, DevOps). CI can also be used to help Quality Assurance. A CI pipeline with automated testing can safeguard from potential issues, and ensure new features are up to specification before they are merged into the final product.

For more information about Continuous Integration and why it is important, Atlassian hosts an [article](https://www.atlassian.com/continuous-delivery/continuous-integration) that goes into detail regarding the subject and DevOps as a whole.

---

### Explain Continuous Delivery and why it is considered important?

Continuous Delivery is the process of delivering changes to software as safely and quickly as possible. A 'change' could be a new feature, a configuration update, a bug fix, or just a developer having fun with the code. The goal is to be able to roll out changes on-demand in a predictable and routine manner. CD is achieved by making sure that even during major development when thousands of changes are being made every single day, the code base itself is always ready for deployment and can deployed on-demand.

When CD is implemented properly, the development team is able to consistently deliver services faster and in a more reliable manner compared to manual workflows. Releasing software carries minimal risk and can be done at any time. For live projects such as websites, specific release patterns such as 'Blue/Green Deployment' can be used to ensure that downtime between releases is virtually undetectable.

When different teams work together to automate testing and building, the relevant stages of the Software Development Life Cycle can be removed from daily work or skipped entirely. This translates to less time between releases, lower overall costs, and avoiding the ongoing revision process of the SDLC. Developers are then able to focus on more important things such as performance and security, overall ensuring higher quality products.

For more information, there are plenty of online materials explaining the importance of Continuous Delivery. There is even an entire website: [continuousdelivery.com](https://continuousdelivery.com/)

---

## References

* [What is Continuous Integration?](https://www.atlassian.com/continuous-delivery/continuous-integration)  
\-Max Rehkopf (Atlassian)  
Retrieved 12 March 2021

* [Continuous Delivery Website](https://continuousdelivery.com/)  
Retrieved 12 March 2021
