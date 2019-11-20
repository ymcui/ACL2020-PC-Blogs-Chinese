# Improving ACL Conflict-of-interest Detection and Reviewer Matching
We all know that ACL conferences are getting bigger, and this is great: reflecting a burgeoning and vigorous community. At the same time, it also means that the amount of work that goes into managing various aspects of the conference is growing greatly as well. In particular, ensuring an effective and fair review process with multiple thousands of papers is a significant challenge that requires a huge amount of work by everyone in the process: from program chairs and area chairs, to reviewers.

To help improve our reviewing process, the ACL organization formed a committee during ACL 2019 to make the review process more effective. One of the first actions of the committee is to move towards improved automation of conflict-of-interest (COI) management and improved (semi-)automation of reviewer-paper matching . The committee has extensively discussed the best way to perform this automation, and produced a report on design decisions that went into this process.

In this blog post, we briefly explain the path we are currently pursuing. This also serves the purpose of explaining why there have been extra steps to set up your profile as potential ACL 2020 reviewers and authors. We welcome any feedback on the process!

## COI Management
ACL has an official policy on what constitutes a COI in reviewing. Specifically, a person has a conflict of interest with a submitted paper if that person:
1. is a co-author of the paper, or 
2. has been a student or supervisor of one of the authors in the previous five years, or 
3. has co-authored a paper or collaborated with one of the authors in the previous five years, or 
4. is employed at the same company or institution as an author, or
5. has any other circumstances that could cause a bias in evaluating the paper.

In order to determine whether COIs exist, we are collecting information from sources including:
1. User profiles in the START system where ACL papers will be submitted. Here conflicts of interest falling under areas #2, #4, or #5 can be manually listed and will be processed by our system. This information will be available only to chairs involved in the organization of the conference, and only when an author or reviewer is added to the conference through submission or indication of willingness to review. 
2. The reviewers’ and authors’ submissions via the START system, and their publications on Semantic Scholar, a large database of academic publications (this allows us to find co-authored papers that were not submitted via START).

The reasons for choosing START (instead of other alternatives such as OpenReview or CMT), and Semantic Scholar (instead of other alternatives such as Google Scholar, the ACL Anthology, or orcid) are discussed thoroughly in the design document

## Reviewer-Paper Matching
In recent years, for \*ACL conferences papers were generally matched to reviewers through a process of first having reviewers bid (“yes”, “no”, “maybe”) on papers, then having area chairs make the final assignments of reviewers to papers. This process is time consuming, and can become difficult to manage for both area chairs and reviewers as conferences grow in size. Recently, \*ACL conferences have experimented with the Toronto Paper Matching System, but this sometimes suffered from lack of coverage due to reviewers not signing up for the system.

This year, we are developing an in-house paper matching system for ACL that aims to create a first-pass reviewer allocation, that area chairs can then go in and modify to create the final assignments. Briefly, the system works by:
1. Gathering papers written in the past by ACL reviewers from Semantic Scholar 
2. Based on the content of the abstracts of (a) papers submitted to ACL, and (b) papers previously written by reviewers, calculate between-paper similarity scores 
3. Create a score for the match between a reviewer and a paper based on the similarity scores for the top few most similar papers that the reviewer has written 
4. Create a reviewer assignment, trying to match reviewers with papers that they are the best fit for, while making sure that no reviewer gets too many (or too few) assignments. 

Based on our experience with ACL 2020, we are considering running a shared task on further improving the efficacy of reviewer allocation algorithms at a later date. We are NLP people, let’s use our skills to improve our processes together!

## What Should You Do?
1. Please complete your START Global User Profile as soon as possible. To do this, log in to START. Then, click on “Update Profile”. Here is a picture of the profile screen:

![screenshot.png](https://acl2020.org/assets/images/profile_update_example.png)

Here is some information from Semantic Scholar about how to find a Semantic Scholar profile ID: One way to do this is to type “Semantic Scholar” and your name into a search engine of your choice, and find the returned profile that corresponds to you. Another option is to find one of your papers on www.semanticscholar.org, and click on your name, or you can search for your name on Semantic Scholar and pick the page with most of your work from the author panel on the right-hand side of the search results.

Semantic Scholar is working closely with us. Here is information from them about what to do if your profile contains errors:

You can add or remove papers by claiming your profile (click on “CLAIM AUTHOR PAGE”) and fix paper details using the “Contact” button on the top right of the page. Feel free to contact Semantic Scholar Support with questions or concerns.

2. If you are interested in reviewing for ACL 2020, or are intending to submit a paper to ACL 2020, please fill out the ACL 2020 author/reviewer survey as soon as possible. 
3. If the program chairs or area chairs contact you with a question about your profile, please respond promptly. 

## Acknowledgments
Amanda and Graham acknowledge the ACL review committee and ACL program chairs for their feedback on this process. They also acknowledge Emily Bender for taking initiative on COI management in START, and Arya McCarthy and John Wieting for their assistance in implementation of COI management and reviewer matching.
