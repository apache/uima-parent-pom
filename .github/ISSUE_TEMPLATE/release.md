---
name: Release (for developers)
about: Prepare a release
---

**Preparations**

- [ ] Create release issue and release preparation branch
- [ ] Make sure to remove all SNAPSHOT repositories and SNAPSHOT dependencies

**Building**

- [ ] Clean local `.m2/repository`
- [ ] Commit all changes and check out in a new clean build location
- [ ] Run a trial build locally with `-Papache-release`
- [ ] Do the release build (`mvn release:prepare release:perform`)

**Staging**

- [ ] Close the staging repository at https://repository.apache.org/ 

**Voting**

- [ ] Call for a vote on the developer mailing list

**Vote**

- [ ] Close vote and post vote results to the developer mailing list (wait at least for 72 hours, at least 3 +1 votes required for release, sign mail using same GPG key that was used to sign release)

**Publishing**

- [ ] Release staging repository at https://repository.apache.org/
- [ ] Create a new git tag e.g. `rel/parent-pom-18` and remove the one not prefixed with `rel`
- [ ] Merge the release preparation pull request
- [ ] Close the release in the issue tracker
