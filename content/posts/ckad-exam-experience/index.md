---
title: "CKAD Exam Experience"
date: 2023-05-08T21:27:49+00:00
draft: true
description: "My experience with Certified Kubernetes Application Developer exam"
tags: ['kubernetes', 'exam', 'ckad', 'helm']
ShowToc: true

cover:
  image: "kubernetes_logo.png"
  responsive: true
  hidden: false
  relative: true
---

Yayy!! 🎉🎉🎉 

I am finally a Certified Kubernetes Application Developer(CKAD).

## Hello Kubernetes, my friend

My first encounter with Kubernetes was at [finleap connect](https://connect.finleap.com). I was building the frontend for [Categorisation](https://connect.finleap.com/categorisation/) platform. The platform used supervised machine learning to categorize transactional data. The Backend and the BFF built on Python, and the Frontend written with React/Redux stack. The platform gets deployed to finleap cloud using kubernetes, something I didn't knew at the time. I wrote my first lines of python using flask as well to create the BFF.  


Kubernetes offers the following benefits. 
1. Scalability
2. High availability
3. Automation
4. Flexibility
5. Portability
6. Resource optimization 

From that time on, I wanted to keep working with Kubernetes as I loved how smooth a rollout process had been. That's when I decided to get the developer certification as a personal goal.


## Exam Experience
All in all, the exam experience was good. The exam happens on the PSI Secure Browser application. A human proctors the exam and communicates using a chat window. The experience is of a remote desktop. The Linux OS GUI was nice and I used Terminal, a notepad, and Firefox Browser. The number of questions vary from 16 to 21. I faced a bit of trouble with the exam as I was on a 14" Macbook Pro. The recommended size is 15" screen. The fonts were bit too small and I had to scroll a lot to see the content on the screen. If you don't have a 15" laptop, I recommend using an external screen and webcam with auto focus feature. I bought a webcam which failed me at the moment of truth. I had to revert back to not so good plan B (use the small screen laptop).


## Post Certification plans 

As of now, I don't know what I am gonna do with the certification. I am proud of myself getting my first certification. I am looking into new roles with possibility of using my Kubernetes skills at the workplace. 

## Tips and Tricks 
Few tips that will help you to pass and get amazing grades in the exam.

1. Practice Practice Practice. It's a hands-on exam and not MCQ.
2. Learn the imperative way of spinning up objects. `kubectl or k(alias)` is your best friend.
3. Good understanding of networking-related topics, especially with services, `NetworkPolicy`, `Ingress` etc.
4. Experience with CRI like `Docker`, `Podman`, `cri-co`.
5. Learn `vi` / `vi` or `nano`. I prefer `vi` and I am in love with how the text editor works. It will help you navigate large docs faster. And trust me, you will forget `Sublime` or `VSCode` once you get the hang of using `vi`.
6. Experience with a terminal emulator. Sounds silly but you must know the tricks to find `history`, using `grep`, `less`, `more`, `yq`. These commands will save you time and effort.
7. Learn and practice `Helm`. Although, the exam contains 1 question from Helm, Helm is the way to go for creating kubernetes apps. We all know the importance of package managers 😉. Saves us a lot of time.
8. Be thorough with networking related topics. Networking is not easy in computers as well as social interactions 😅. I could not solve one question related to networking. Also because, in CKAD, you don't need much hands-on for networking topics but the exam will test you.
9. For the exam, a 15"+ screen is the recommendation. I attempted my exam on a 14" screen and it turned out to be very difficult to navigate and switch between applications inside the remote desktop environment


