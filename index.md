---
title: Design Debt Economics
subtitle: A vocabulary for describing the causes, costs, and cures for software maintainability problems
author: John Elm
date: 2009-06-12
source: The Rational Edge / IBM developerWorks
---
> 📄 [Download PDF version](./design_debt_economics.pdf)

# {{ page.title }}

*{{ page.subtitle }}*

*From The Rational Edge:* Code maintainability is vitally important to software quality and is relevant to all development stakeholders. This article explains the impacts of code maintainability problems and how to identify and mitigate them.

**John Elm** was an Advisory Software Engineer in IBM's Global Business Services. At publication time, he had 17 years' experience in information technology as a developer, designer, and team leader, and as a continuous integration and configuration management specialist. He advocates for the technical vitality of organizations and individuals, with a penchant for building organizational capability. John is also a semi-professional musician, and enjoys playing softball and riding his motorcycle in his spare time.

*12 June 2009*

> On many application development teams, the ongoing choices, actions, and practices of team members can have a negative impact on code maintainability and hence overall code quality. Until these issues are discerned and tended to, they will become more and more costly, in terms of increasing the time required to perform changes and in ongoing developer resource cost. Further, risk of regression defects increases when code maintainability is compromised, because code that is not properly maintained is inherently more brittle.

This article underscores the importance of code maintainability for application owners and development teams, describes the future impacts of neglecting code maintainability problems, attempts to impart an appropriate sense of urgency for resolving such problems where they are found, and presents some proven solutions.

## Design debt and code maintainability

Where code maintainability problems exist, it is entirely possible that the issue has not been observed by the casual onlooker, or by the typical user, since the maintainability issue is internal to the application. Indeed, while the internal structure of the code that comprises the application is incommodious to change and difficult to trace, externally the system may fulfill its functional requirements well.

In this article, I use a financial metaphor, *design debt*, to show the importance of code maintainability. This metaphor emphasizes that unmaintainable code is costly, especially when changes are performed that go beyond the superficial, and when it is necessary to train new staff for a maintenance or development role for the application. Design debt is, broadly, the degree to which application code is problematic to maintain because it contains excessive duplication, is overly complex, and/or is inordinately difficult to understand when viewed by human eyes. The design debt metaphor goes beyond describing the cost of unmaintainable code, that is, interest payments. It also underscores the importance of the actions that result in unmaintainable code, withdrawals, and those that improve the maintainability of that code, repayment.

Design debt results when a development team is not skilled in, committed to, and discerning about code quality practices. It may also result if the team is unable to establish or adhere to code quality best practices, due to time constraints or other overriding priorities. Typically, code quality best practices are much more difficult to establish after a project is underway than at the beginning.

## Solutions

If the design debt issue is to be resolved, a three-pronged approach should be employed.

First, design debt must be acknowledged, enumerated, and monitored.

Next, so that the design debt withdrawals can stop, the development team must attain the ability to write more maintainable code. To do this, a culture of quality must be fostered wherein everyone has the skills and the commitment to perform best practices that ensure the consistent production of high-quality, maintainable work products. More emphasis must be placed on the internal design and structure of the application, rather than merely achieving the external fulfillment of functional requirements. The customer and the team's body of governance should be aware and engaged. It is critical that the team is supported, empowered, and accountable to establish a culture that values and rewards quality.

Third, the existing design debt must be reduced. The application must be brought closer to the ideal of highly maintainable code, either by improving the code's maintainability, or by replacing it with code that is more maintainable. While the latter sounds like a lot more work, this is not necessarily true. When design debt is extreme, it is often faster and less risky to rewrite the debt-ridden body of code than to attempt to improve it. Either way, the internals of the application would be improved, while externally, the existing functionality would be preserved.

## Recommended strategy for implementing a solution

The recommended solution to the code maintainability issue just described is a *skills vitality* strategy aimed at establishing a *ubiquitous culture of software quality*. This strategy is discussed in the remainder of this article.

## Putting design debt in perspective

Design debt is, broadly, the degree to which application code is unmaintainable, because it contains much duplication, is overly complex, or is inordinately difficult to understand when viewed by human eyes. The design debt metaphor was first used by Ward Cunningham in his OOPSLA 1992 experience report,[^1] where he described the common practice of using a little temporary debt to speed up development. Martin Fowler referred to it in *Refactoring*.[^2] Joshua Kerievsky elaborates on design debt in *Refactoring to Patterns*.[^3][^4]

Any time we do something in code that is not in the interest of the application's ongoing maintainability, we incur some design debt. Each of these withdrawals puts distance between the project we're working on and the ideal of highly maintainable code.

### Design debt has its place

Design debt actually has its place. Sometimes, knowingly incurring some debt is the right thing to do, and a small withdrawal can help relieve short-term time and/or resource pressures. Whenever we knowingly incur debt, we should capture a record of the withdrawal, and schedule repayment. Tracking tools like IBM Rational Team Concert make it easy to create, categorize, and schedule repayment for design debt work items.

### Unmanaged design debt

What is far more concerning, and sadly, more common, is design debt that is unacknowledged and unmanaged. Just as with design debt's real-life financial analogy, there is an ongoing cost to service design debt, because of the impact on code maintainability. The interest that we pay on design debt is additional cost every time we have to change or add functionality, and every time we must acclimate somebody new to the development team.

A metaphor though it is, the real bottom-line costs of design debt cannot be ignored. Author and software consultant Joshua Kerievsky helps explain the literal truth of design debt. This quote is in the context of compound interest:

> Due to ignorance or a commitment to "not fix what ain't broken," many programmers and teams spend little time paying down design debt.
>
> In financial terms, if you don't pay off a debt, you incur late fees. If you don't pay your late fees, you incur higher late fees. The more you don't pay, the worse your fees and payments become. Compound interest kicks in, and as time goes on, getting out of debt becomes an impossible dream. So it is with design debt.[^5]

The most common reasons for unmanaged design debt, gathered from my experience and from numerous industry anecdotes, are:

- Time pressure
- Lack of skills, ignorance, or apathy
- Isolated or disconnected teams, or lack of quality feedback
- Inadequate standards
- Programmer and management hesitance to improving code, for fear of introducing new problems: "If it ain't broke, don't fix it."

## What to do about design debt

As mentioned above, dealing with design debt requires a three-pronged approach:

1. Enumerate and track the debt
2. Stop the bleeding, that is, stop making withdrawals
3. Settle up, that is, reduce or eliminate the debt

### Tracking design debt

Once the issue of design debt is acknowledged, debt should be recorded whenever it is incurred or identified. The backlog should be monitored, the items prioritized, and debt repayment should be scheduled, just as the remediations for functional defects are, in release plans.

Defect tracking tools like Rational Team Concert are the most effective way to track design debt, because they provide reporting and visibility to the design debt backlog, and they support the necessary workflow for assigning the debt items and performing repayment. Rational Team Concert also provides for collaboration about the debt items and their remediations. This can be very useful and educational for all of the developers involved.

The defect tracker chosen for tracking design debt should be fast and easy to use, and it should accommodate rapid capture. If the tracker used is difficult to use, too rigorous, or it "pushes back," then design debt will not be captured whenever it is encountered. It may be a consideration to use a separate defect tracker from the customer and the testers, if it is necessary to accommodate this lightweight, rapid capture of design debt.

Design debt can be set apart by tagging it with a `design-debt` designation, or by using a distinct work item type. This can be helpful if the customer and test organization does not wish to have constant visibility to design debt activity. Since design debt is technical and not functional in nature, this activity may be considered noisy to non-developers. Ideally, the intention should not be to hide design debt from the customer, as I discuss later in this paper. In any case, if design debt is going to be managed and tracked, the development team must be able to capture design debt records without fear, hesitation, or resistance of any kind.

### Stop the bleeding, stop making withdrawals

When any team comes to realize that it has been incurring great design debt, the first thing they must do is get control over the withdrawals. The team must have the ability and the commitment to write more maintainable code.

#### Foster a culture of software quality

To do this, a culture of quality must be fostered that will immerse and surround all development activities on the team. An atmosphere must be created wherein design debt withdrawals are conspicuous and stand out as the outliers, rather than being accepted as the norm. More attention must be paid to the internal quality of code, and the definition of delivery excellence should be broadened so that it includes maintainability, not merely delivering on functional requirements.

Today, such a culture is usually marked by these practices and more:

- Test Driven Development (TDD)
- Continuous refactoring, typically enabled by TDD
- Continuous Integration
- Adherence to coding standards
- Design patterns
- Domain driven design
- Peer review
- Reflection and lessons learned

In order for a team to stop making uncontrolled withdrawals, it will need to ratify its commitment to selected best practices, and make them pervasive on the project.

A good place to start is with a preliminary exercise to determine which practices the team will adopt, or readopt more formally, and then decide on roles, responsibilities, measures, and tool support.[^6][^7] Where there are multiple applications, especially legacy applications, it may not be practical to treat them all exactly the same. Some of the practices are very difficult to apply to a body of code that was not written using the practice. Therefore, tailoring the use of the practices on a component-by-component basis should be a consideration.

#### Holistic approach to skills

We should not solely regard technical skills like application frameworks, Java Database Connectivity (JDBC), and Servlets, as critical skills for our developers. We must further encourage, support, and require the development of "soft-technical" skills that support the culture of quality and produce highly maintainable code. Among these skills would be writing readable code, recognizing code smells,[^8] leveraging design patterns, plus many of the practices mentioned above, especially Test Driven Development.

Teams should taxonomize the skills that are important for their success as quality-driven units, and support the development of these skills via evaluation, mentoring, lunch-and-learn sessions, and more. Team members should naturally include these skills in their training budgets and skills planning.

#### Agile methodologies and practices

One of the most effective ways to establish a culture of quality is through the formal adoption of an agile methodology, like OpenUP, RUP@Scale, Scrum, Extreme Programming (XP), or Eclipse Way. The full involvement and support of the customer and management is critical for such an adoption. An investment in skills and enablement is also necessary, but it is well worth it. Some supporting tracking and collaboration tools like Rational Team Concert should be considered as well. Today, there is much support for Agile adoption in the form of education, conferences, communities, articles, consultants, coaches, and more.[^9]

Where a formal agile adoption is not possible, there can still be worthwhile benefit from "grassroots" adoption of selected Agile practices on the part of the development team. Increased quality, and enthusiasm about quality, will certainly result. There are many anecdotes of full-on Agile adoptions that began with technically vital developers who began performing selected Agile practices in this way.

#### The role of application frameworks

There are many application development frameworks available, most of them open source, which can be very helpful in avoiding duplication, maintaining layered architectures, and in promoting loose coupling and testability. They can also aid in the adoption of beneficial or desirable programming techniques like Aspect Oriented Programming (AOP) and asynchronous JavaScript and XML (AJAX). Examples of these frameworks include:

- Spring and Google Guice, for Dependency Injection
- Spring-AOP and AspectJ, for Aspect Oriented Programming
- Hibernate and iBatis, for object-relational mapping and database abstraction
- JavaServer Faces (JSF) implementations and plugins like MyFaces, Ajax4JSF, RichFaces, and Facelets

Using frameworks like these can greatly enhance application maintainability and quality for the long term.[^10][^11]

#### Governance

Once the practices and tools are settled, they should become ratified decisions, for example, in a team charter; and an accountability framework should be created, including reporting and monitoring. Anyone that touches code, or who has oversight over code, must be committed to ensuring that the practices are performed according to the charter. According to Jeanne W. Ross and Peter Weill:

> Governance is the assignment of decision rights and the accountability framework to encourage desirable behaviors in Information Technology.[^12]

The role of governance for ensuring long-term persistence of a culture of software quality should be considered. By using a team charter to make team members accountable, the team is exercising a team-local, feudal right to decide what they believe is right for their applications and what is best for the customer, when it comes to software quality practices. If there exists a portfolio architect or technical leadership body with high-level architectural oversight, they should be engaged to assert and confirm this feudal right, and their support should be entreated. Involving or invoking such technical leadership can achieve accountability outside the local team, to ensure that the quality culture endures, even if staff changes occur.

Governance is also one mechanism by which a culture of software quality can and should be broadened. Colleagues' projects may also have the opportunity to benefit from local experience. Technical leadership can facilitate this sharing, and can begin to observe design debt and how it is handled among various projects. Synergy can be realized by sharing anecdotes, papers, skills attainment methods, and test fixtures.

#### Involve management and the customer

The ubiquity of the quality culture should extend to the customer. The customer should be educated about the concepts of design debt economics, and open, candid dialogs should be encouraged. If the customer understands design debt, it is much easier to articulate the need to pay it back, and organizations can better avoid incurring inordinate debt caused by short-term time pressure.

Kerievsky uses the design debt analogy to communicate with managers:

> Discussing technical problems using the financial metaphor of design debt is a proven way to get through to management. I routinely take out a credit card and show it to managers when I'm speaking about design debt. I ask them, "How many months in a row do you not pay down your debt?" While some do not always pay off their debt in full each month, nearly all do not let debt accumulate for long. Discussions like this help managers acknowledge the wisdom of continuously paying down design debt. Once management accepts the importance of keeping design debt under control, the organization's entire way of building software can change. Suddenly, everyone from executives to managers to programmers agrees that going too fast hurts everyone. Programmers now have management's blessing to refactor. Over time, the small, hygienic acts of refactoring accumulate to make systems easier and easier to extend and maintain. When that happens, everyone benefits, including the makers, managers, and users of the software.[^13]

When more significant effort becomes necessary to deal with design debt, this vocabulary can also be helpful when demonstrating the need to customers and stakeholders, especially if they are familiar with it beforehand.

Of course, such dialog need not represent that a poor job has been done for the customer. There is not a development team in the world that does not deal with design debt, though it may be doing so unknowingly. Again, design debt is reflected by poor code maintainability, and the internal structure of an application, but the external manifestation is probably an application that fulfills the customer's requirements well. We can, however, improve on our stewardship of our customer's code assets by better protecting and guiding their investments.

### Settle up, eliminate the debt

The most obvious solution to design debt is to "pay it back."

#### Refactor, and do not stop

Once design debt has been identified and logged, repayment via refactoring should certainly be made a priority. Refactoring is the act of improving the internal structure of code without changing its external behavior.[^14]

Refactoring can be performed to improve the code in these ways:

- Improve readability, making code self-documenting wherever possible[^15]
- Establish better layering and effectively employ enterprise architecture patterns
- Establish higher testability and greater test coverage
- More besides

Continuous refactoring should carry on as an ongoing activity, to look after the small intentional and unintentional withdrawals that every development team invariably makes. Without ongoing, continuous refactoring, design debt will again accumulate.

#### Tackling large legacy code bases: divide and conquer

Improving the maintainability of a large legacy code base can be very difficult, especially where there is no layering or identifiable structure. One effective refactoring strategy is to introduce to the application a dependency injection container like Spring or Google Guice.[^16] Then, gradually, application functionality can be abstracted into services, which are managed via dependency injection and which reside in a proper service layer. Better layering, looser coupling, and greater testability can be achieved over time by performing these refactorings.

With each round of this refactoring, the external functionality of the application remains unchanged. Therefore, the improvements can be performed incrementally across multiple releases. This can be one way to improve an architecture in cases where significant time for refactoring cannot be budgeted.

This approach might be analogous to establishing a stronghold within the code, from which you can launch small sorties of refactoring to divide and conquer the maintainability problems. Every small victory will make subsequent battles less bloody.

#### Bankruptcy

It is always very difficult to improve the maintainability of a codebase which was not written to be maintainable. This is a thwarting Catch-22: code needs to be maintainable, with adequate test coverage, in order to safely apply wholesale change, but we cannot improve its maintainability without refactoring, that is, changing it. This is why many projects designed to improve the quality of legacy applications fail to do so.

So, when a team finds itself in great design debt, it may be time for some tough decisions. It should be considered that the cost of improving the existing code in an application may indeed be greater than the cost of rewriting it.[^17] Within the design debt vocabulary, such a rewrite might be likened to "declaring bankruptcy," but ironically, this can be the most responsible course of action, since the debt is really owed to us and to our customer.

Rewriting an application module is not necessarily starting from scratch. The team likely has significant experience with the current implementation and the business. In addition, they have probably learned a greater ability to write quality, maintainable applications, and there are better frameworks and tools at their disposal.

Notions about application rewrites are often unpopular. The bottom line is that in order to avoid them, design debt must be regarded and respected early enough that bankruptcy is not risked. Ideally, design debt should be managed right from the beginning of development projects.

#### Big Ball of Mud (BBoM)

Here is how to identify that an application is at the verge of bankruptcy: small enhancements and superficial changes are doable, but larger changes are very difficult, often requiring expensive rediscovery of winding paths of spaghetti code. Brian Foote and Joseph Yoder wrote a very well-known article on this state of affairs, calling it "Big Ball of Mud". Wikipedia describes "Big Ball of Mud" as an anti-pattern: "a system without a recognizable structure."[^18] Here is Foote and Yoder's definition:[^19]

> A Big Ball of Mud is a haphazardly structured, sprawling, sloppy, duct-tape-and-baling-wire, spaghetti-code jungle. These systems show unmistakable signs of unregulated growth, and repeated, expedient repair. Information is shared promiscuously among distant elements of the system, often to the point where nearly all the important information becomes global or duplicated. The overall structure of the system may never have been well defined. If it was, it may have eroded beyond recognition. Programmers with a shred of architectural sensibility shun these quagmires. Only those who are unconcerned about architecture, and, perhaps, are comfortable with the inertia of the day-to-day chore of patching the holes in these failing dikes, are content to work on such systems.

Wikipedia's entry on Big Ball of Mud also describes it very well, with a notable exhortation:

> Programmers in control of a big ball of mud project are strongly encouraged to study it and to understand what it accomplishes and use this as a loose basis for a formal set of requirements for the new well architected system that would be developed to replace the former. Technology shifts, client-server to web-based, file-based to database-based, and so on, can provide good reasons to start over from scratch.[^20]

## Summary

The long-term costs of ignorance, apathy, or inaction about code maintainability problems are very high. The vocabulary of design debt can be helpful in articulating the long-term costs, causes, and cures of code quality problems in honest, candid conversations with management, customers, and colleagues.

To resolve code quality problems, it is necessary to foster a culture of software quality, through a holistic skills vitality strategy, through software quality practices, and by using frameworks that are proven to promote code quality and maintainability.

Sometimes, when code maintainability problems are insurmountable, tough decisions must be made. The sooner teams start managing design debt, the more likely it is that they can avoid paying interest that they would rather not pay. Thomas J. Watson, Chairman of IBM from 1949 to 1956, articulated this truth with elegant simplicity: "Good design is good business."

## Author's note

I wrote this article because I frequently find myself trying to articulate the long-term cost of decisions often made to save cost in the short term. I wanted to bring some compelling arguments into those discussions, and to support more foresight about software development practices. While doing that, I also tried to provide a glimpse of a team culture where software quality practices prevail.

Shortly before this article was published in *The Rational Edge*, I picked up a copy of *Clean Code: A Handbook of Agile Software Craftsmanship*, the brand new book by Robert C. ("Uncle Bob") Martin and the other authors at Object Mentor, Inc.[^21]

At the beginning of *Clean Code*, Uncle Bob addresses "The Total Cost of Owning a Mess," a discussion that is entirely congruent with the design debt metaphor in this article. From there, he and his co-authors proceed to provide a detailed, comprehensive treatment of code quality topics.

I strongly recommend reading *Clean Code* in its entirety. If you are on a development team and agree broadly with the recommendations in this paper, and you seek more concrete, practical advice for proceeding, *Clean Code* belongs near the top of your reading list and is a great follow-on read from here.

[^1]: http://c2.com/doc/oopsla92.html
[^2]: Martin Fowler, *Refactoring*, Addison-Wesley Longman Inc., 1999, p. 66.
[^3]: Joshua Kerievsky, *Refactoring to Patterns*, Pearson Education Inc., 2005, pp. 15-16.
[^4]: A sample chapter of Kerievsky (2005), including the sections on design debt and on writing human-readable code, is online at http://www.informit.com/articles/article.aspx?p=360842
[^5]: Kerievsky, p. 16.
[^6]: Many of these practices were developed and proven in the Open Source and Agile communities. They are sometimes referred to as "methods" but it is more accurate to recognize that the practices can be constituents of broader Agile methodologies. In other words, each Agile method, for example OpenUP, RUP@Scale, Scrum, Eclipse Way, or XP, prescribes a selection of practices along with specific process guidance. Regardless, the practices can offer great dividends in quality, whether adopted on their own or as part of a broader, more formal method adoption.
[^7]: Tools that perform static code analysis, like IBM Rational Software Architect and IBM Rational Software Analyzer, can identify common problems in code and, in many cases, can resolve them quickly by offering "quick fixes" that can be applied with a simple menu command.
[^8]: A code smell is an indicator of maintainability problems in code: http://c2.com/xp/CodeSmell.html. There are many great references on code smells online, and also in Fowler (1999), pp. 75-88, Kerievsky (2005), pp. 37-45, and Martin (2009), pp. 285-315.
[^9]: Agile teams that use Rational Team Concert can benefit greatly from the guidance in the included process templates. Scrum, Eclipse Way, OpenUP, and more are supported.
[^10]: JSF and Spring are both examples of "hub" technologies, each sporting a plug-in architecture that puts many sub-frameworks within easy reach. For example, AOP, declarative transaction management, and more are easy to adopt by coding to Spring's abstractions of these technologies. Spring's abstraction layers also make many technologies virtually swappable while hiding the implementation complexities.
[^11]: In addition to software quality practices, it is my experience that where you find these frameworks, you frequently also find highly maintainable code, written by developers who are skilled and enthusiastic about application and process quality. Conversely, I do not recall noting such a culture where these frameworks were entirely absent, in recent times. I look for investments in frameworks like these as one likely sign of a culture of software quality.
[^12]: See the Ross and Weill paper on IT governance at http://papers.ssrn.com/sol3/papers.cfm?abstract_id=664612
[^13]: Kerievsky (2005), p. 16.
[^14]: See Martin Fowler's refactoring website at http://www.refactoring.com, and Fowler (1999).
[^15]: Self-documenting code is not code with lots of inline comments. This is a common misconception, and indeed a misnomer: spuriously commented code is documented, but by a developer, not by the code itself. Conversely, self-documenting code is running code that is readable and easily understood by an observing developer, so that its intents, purposes, and techniques are clear without supplemental comments. Comments are valuable and often necessary, but self-documenting code is more desirable because it is guaranteed to remain current: comments can become stale and misleading, but running code does not lie.
[^16]: Dependency Injection is a software pattern that is usually implemented through the use of frameworks like Spring. It accommodates and enforces the loose coupling of application components, which leads to better maintainability, testability, and overall quality. See http://www.martinfowler.com/articles/injection.html and http://en.wikipedia.org/wiki/Dependency_injection
[^17]: I believe there are three factors which may justify keeping a badly debt-ridden codebase: (1) low backlog and low volume of anticipated change, (2) very few developers required for development and maintenance, and (3) low staff turnover. If all of these items remain very low, so does the interest paid on the debt.
[^18]: An anti-pattern is a commonly reinvented or commonly reoccurring bad solution to a problem. See http://en.wikipedia.org/wiki/Anti-pattern (BBoM is listed here).
[^19]: The Big Ball of Mud paper by Foote and Yoder is online at http://www.laputan.org/mud/
[^20]: http://en.wikipedia.org/wiki/Big_ball_of_mud
[^21]: Robert C. Martin, *Clean Code: A Handbook of Agile Software Craftsmanship*, Pearson Education Inc., 2009.
