# Review

## Info

Reviewer Name: John Nickels

Paper Title: Protection

Paper Author: Lampson

## Summary
    In this paper, the author seeks to introduce a set of abstract models, 
    as well as some implementation hints, for ensuring the protection of a 
    program from other things in the system. To this end, the author 
    introduces the concepts of Protection Domains, Access Control Matrices, 
    and Memory Protection, which reflect several now-standard cybersecurity 
    practices.

### Problem and why we care
    When different programs run on the same machine, there is inevitably 
    going to be some conflict between those different programs, including 
    their demand for limited resources, need for private memory access, and 
    protection from other user's/program's errors, to say nothing of malicious 
    activities. As defined in this paper, Protection is necessary to limit 
    these conflicts and allow different programs to cooperate to complete 
    their tasks.
    
### Gap in current approaches
    At the time, protection was generally a collection of ad hoc mechanisms 
    designed to solve specific issues. While this approach will solve 
    individual issues, some higher order models are needed to organize and 
    standardize approaches to protection. 
    
### Key Idea
    In order to protect a program from other programs on the same machine, 
    the system should be designed with three protection concepts in mind:
    
        1. Protection Domains- by logically seperating the domain of a 'user', 
        or a program, from other users and from the supervisor (kernel), we can 
        begin to build an idea of what's being protected and who has the power 
        to take certain actions.
        
        2. Access Control Matrix- once a concept of identity has been created, 
        an Access Control Matrix can associate that identity with a set of access 
        attributes, allowing the supervisor to enforce limitations on what certain 
        programs can do with certain things (eg, read, write, execute, etc.).
        
        3. Memory Protection- once it can be determined if a certain access should 
        be allowed, there needs to be some protections to allow legal accesses and 
        deny illegal ones. 
        
### Method for Proving the Claim/Evaluation
    This paper is an abstract discussion of protection principles, and has no 
    prototype to evaluate. Therefore, the author seeks only to defend his key ideas 
    through a mathematically-styled proof. He will introduce a concept such as an 
    Access Control Matrix, then discuss how it is able to prevent the threat vector 
    it addresses. 
    
### Contributions: what we take away
    It appears as if Lampson's paper is the origin of the Access Control Matrix, a 
    fundamental of cybersecurity. Furthermore, although not an original idea, the 
    concept of a protection domain lives on both in the user-mode/kernel-mode dichotomy 
    and in the modern concept of a process.

## Pros 

    - Protection domains have been proven to be a very effective tool in protecting a 
    program's exectution environment
    
    - Access Control Lists, and the corollated capabilities, have continued to be tools 
    used in managing permissions in modern security.
    
    - All of the mechanisms discussed require no modification to the programs, but only 
    to the environment, which leads to easier development forced participation for the
    programs.
    
## Cons 

    - There's no demonstration of his ideas, which limits the conclusions that could be 
    drawn at the time.
    
    - Many of the proposed ideas are somewhat outdated at this point, and are too cumbersome 
    for modern systems.
    
    - The proposed models add significant complexity, energy, runtime, and memory usage to 
    the system.
        
### What is your analysis of the proposal?
    The proposed solution is rather high level, which limits the conclusions that can be 
    drawn from it when limited to the context of the time. That said, the ideas proposed 
    here have shown up in modern systems enough to demonstrate their merit. I think that 
    with paper like this that discusses now-accepted fundamentals of a field, it is especially 
    difficult to critically evaluate it, especially in the context in which it was proposed. 

## Details Comments, Observations, Questions
    This paper feels like a fundamental introduction to the idea of protecting a computer, 
    and one that I think belongs near the beginning of the class. It introduces some very 
    important models that we have been using throughout the class, and does a good job of defining 
    the original goal of protection, and hints at its evolution into what we think of as modern 
    security. It was certainly interesting to see the Access Control matrix being proposed as a 
    new idea, given how engrained it is today.
