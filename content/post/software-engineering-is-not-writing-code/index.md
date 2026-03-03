---
date: "2026-03-03T18:33:16+01:00"
draft: true
title: "Software Engineering Is Not Writing Code"
description: |-
    That's true, being a software engineer is not only converting caffeine into
    code. Most of the work is not descripted in any book, is lived everyday by
    experience. I have found an article from Addy Osmani, a Google software
    engineer, and I want to express my thoughts about it. I think it's a very good
    article, and I want to share my opinion from a different experience on few
    of the points that Addy talks about.
---


This is an interesting article from 
[Addy Osmani Blog](https://addyosmani.com/blog/21-lessons/)


## The hidden problem

Everybody prefer a tecnology over another one, I have my preferences, and I
like making things in a certain way, with specific patterns and tools. I've
always seached for the best way to do things to understand finally that `it
depends`. Why depends? Each time I'm writing a piece of software the most
important thing is not the code itself, but the problem that I'm trying to
solve. The `hidden problem` to solve to be precise.

![thinking-programmer](./thinking-programmer.jpg)

There's always someone that bring you a "complete" solution.  The first question
to make him is "which is the problem to solve?". If no aswer, the solution is
pure garbage, it won't work at all.

The problem shows the solution, the solution decide the technology, starting in
the middle of this chain, is a recipe for disaster. I have seen many times
people that start to write (me included) without understanding the problem, and
they end up with a perfect software, a perfect code, clean too, but the users
hate it. 

Stop, `listen` and understand the needs.

People are not prepared to express the real problem, they don't know how to
tell their needs, and you should listen to them to look for the hidden small
details, the untold conversations, those small automatic tiny steps they make
automatically.

As Addy said, "The solution should emerge from that understanding", when the
problem is totally clear, the solution is just a consequence of it, and the
technology came after. It's not an obsession about research, it's about be sure
to fully understand the needs. 

This is not being a "best engineer", this is being a good one, a software
engineer that programs things once to be used by people everyday without lots of
fix and changes.

## Fail fast, fail safe

> You can edit a bad page, but you can't edit a blank one.
> The quest for perfection is paralysing

Never agreed more with a quote. I was a "bad" perfectionist, I wanted to write
the best code, the best design, the best architecture, but the result was I lost
of focus, and a lost of objective. What I've learned is summarized in this old
IPad commercial.

<iframe width="560" height="315"
src="https://www.youtube.com/embed/1I1hVBOPVkQ?si=A_IYea3ifW5uMFEi"
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay;
clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

You can create the best software ever but only when you give it to a user you will
see if works well and how he's using it. You can have the best design, but if
people don't understand how to use it, it's useless, it has no value. If you
show something to people and listen to their feedback, you will understand if
you are in the right direction.

Fast deployments, and fast feedback. 

This doesn't mean "deploy hard broken features" to production, but it means that
you shouldn't be afraid to ship something that is not perfect to make it be
tested. This allows more to understand people needs and to make the software
evolve in the right direction.

> Our highest priority is to satisfy the customer
> through early and continuous delivery of valuable software.

from [Agile manifesto principles](https://agilemanifesto.org/principles.html)

Monitoring and understanding if the problem is correctly solved guide next steps
of software evolution to a fix or to a new feature. Continuesly building new
feature being blind if everything already done is used as we designed it too.
Understaing user sadisfaction is the key to success, and that is only possible
giving people cutting boards to use!


## The best thing you can do it avoid writing code

I think I agree with the quote

> The best code is the code you never had to write.

but for a different reason. Addy is talking about the fact that if you can avoid
writing code, you should do it, because writing code is a risk, it's a source of
bugs, and it's a source of maintenance. 

Everything true, I agree with that but I think the best code is the code that
you never had to write because you can solve the problem in a totally different
way, without writing code at all. There are so many thing out there, so many
different software and tools that can me adapted to solve the problem without
writing a single line of code.

Most of the problems I faced with are not real software requirements, the
problem is hidden in the process, in the way people are doing it. Few years ago
I had lots of helpdesk tickets about a broken feature of a software. It was a
mess and was very difficult to understand the code and debug it. I decided to do
escalation of the problem talking directly to the users. I've substituted the
feature with a simple report created ad-hoc for that users and deleted the
feature. Everyone was happy, the users had what they needed, and I didn't have
to maintain something bad.

Focusing on the moon instead of the finger helps to find a better solution, and
sometimes the best solution is not writing code at all, it's only thinking about
the process and discuss with people to find a better way to achieve the same
goal.

This concept goes well with usign a new technology to do the job. Are you
putting an home made cache solution or do you prefer to use Redis? Are you using
queues to do some background processing or do you prefer to use a service like
AWS SQS or RabbitMQ? Of course, it's technical debt, but it's a technical debt
that can be managable with small effort instead of inventing a new wheel and
maintain it for years.

You should be sure that you can manage and comprehend the new technology, it
can't be a leap of faith. Every technical debt is a loan, and you should be sure
that you can repay it in the future with paying fees of understanding and
knoledge. Make baby steps in adopting new technologies but is important to move
on a little bit. 

Fossilizing on the same technology is a technical debt too, it's a loan that you
are taking to avoid the cognitive overhead of learning and do something new, but
you should be sure that you can repay it in the future when the updating of the
software is needed.


