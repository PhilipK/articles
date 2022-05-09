# Complexity is the mind killer
TL;DR: When faced with a choice, always pick the simplest thing that solves your immediate problem. Then make sure you can change your mind later. By the simplest thing I mean the solution that is easiest to reason about.

When we always pick the simplest solution we avoid the analysis paralysis of finding out which solution might be the best in all the future scenarios we can imagine. We simply pick the simplest thing, and move on, knowing that it is easy to change our mind later. After we implement the simple solution, we have a much better understanding of our problem and we can ask "is my immediate problem solved?" If not; repeat. 

Complexity is the mind killer. Our mind gets overloaded when we try to change a complex system, and this causes us to make mistakes. Systems must be changeable, it is what keeps them from becoming legacy and it keeps us agile and adaptable. 

A lot of complexity gets added in the name of changeability. We create microservice systems so we can change our programming language and service implementation, but we add the complexity of network, service discovery, message queues, container orchestration and so on. 
It also adds a resource overhead that forces us to scale horizontally earlier, which is complex.
Could we simply have hidden the implementation behind an interface or a function? Will we actually change our programming language any time soon? Does it actually solve our immediate problem?

Always look at the scale of your immediate problem to find your simplest thing. Here are some common complexity traps: 
* When you have to store some data, don’t rush to set up a database right away. A database adds the complexity of network, sql, schemas, deadlocks and so on. Could you just save it as files on disk or even in memory? 
* Do you need to use that framework or library? Or could you implement the one function you actually use yourself? 
* Do you need CQRS, N-Tier, Redux or MVC architecture? Do they actually solve your immediate problem or are they just added complexity right now? 
* Do you need to refactor your code? Or are you trying to make it “prettier” and more changeable for a future that might never happen?

The simplest solution is often the fastest to implement. This lets us iterate faster, which leads to faster feedback, which leads to a better solution in general. Be okay with deleting your code. The less time you invest in it, the less it hurts to delete. Avoid the temptation to add a “quick fix” to a flawed abstraction. Just delete it, and write something that encapsulates your new abstraction simply. If it is simple, it is fast to rewrite.

Unlike other engineering fields, software is always changeable! Use that power by picking the simplest thing that solves your immediate problem, and then change it when it is needed.
