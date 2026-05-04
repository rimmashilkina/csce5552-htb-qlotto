# Hack The Box: QLotto

## Course
CSCE 5552

## Group
Group 1: Garrick Mcculler, Haven Guililat, James Horsman, Rimma Shilkina

## Challenge Overview
QLotto is a network-based Hack The Box challenge where the service is accessed through a TCP connection using Netcat.

## Vulnerability
The application blocks index 0, but it does not properly sanitize negative indices. In Python, negative indices wrap around, allowing access to protected qubits.

## Exploitation
By using negative indices, we were able to control both qubits and make the lottery output predictable.

## Formula Used
lotto = (63 - (n - 1)) % 42 + 1

## Final Answer
21, 8, 23, 30, 13, 10

## Takeaway
Small input-validation mistakes can completely break the security of an application.

## Presentation
[Link](https://github.com/rimmashilkina/csce5552-htb-qlotto-writeup/blob/878707f5e4b6bf25ae81683fadf6232ea546076e/CSCE%205552%20Hack%20the%20Box(Group%201).pptx)
