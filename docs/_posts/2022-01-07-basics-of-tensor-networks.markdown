---
layout: post
title:  "Basics of Tensor Networks"
date:   2022-01-07 15:47:04 -0500
categories: jekyll update
---
I'm currently reading [an introduction to tensor networks by Roman Orus][tn-review]. Previously I was introduced to matrix product states (MPS) in a quantum information class, but I have never learned about tensor networks in depth before. First, I'll give a general overview of the benefits and challenges of tensor networks, then I'll dive into more involved details.

Tensor networks are a condensed way of representing a quantum state without storing the $$p^n$$ wavefunction coefficients, where $$p$$ is the dimension of a qudit and $$n$$ is the number of qudits. The method of encoding the state in locally connected tensors naturally encodes the entanglement structure of the state, and works particularly well for states without long-range entanglement. In one dimension, where the MPS representation efficiently can encode all states with area law entanglement, which includes all thermal and ground states of gapped Hamiltonians in 1D. 

The general data structure for a tensor network is a graph: onsite tensors and bond tensors (represented by nodes) and edges, which represent contracting tensor indices.  

While tensor networks cut down on the space required to store a quantum state, the time required to contract a tensor network can be unwieldy in general. A one-dimensional MPS can be contracted efficiently . However, in two dimensions, contracting a PEPS is #P hard. As a reminder, #P involves counting the solutions to NP-Complete problems, so it encompasses all of NP.  

[tn-review]: https://arxiv.org/pdf/1306.2164.pdf
