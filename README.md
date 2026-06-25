# FINC: Short-Window Fully In-Network Classification on the Programmable Data Plane

This is the official repository for the paper: 

> **FINC: Short-Window Fully In-Network Classification on the Programmable Data Plane**  
> Lior Shafir, Raja Giryes, Avishai Wool (Tel Aviv University)


In this repository you will find the code of our P4 implementation, offline training and
evaluation, data plane compiler and data reprocessing method coupled with the
packet-level labeled version of these dataset.

## Overview

FINC is a novel Fully In-Network traffic Classification approach for the P4 programmable data plane. The system is designed to allow per-packet machine learning (ML) inference without the need to wait for the flow to terminate, enabling accurate early detection: the classification decision is made based on a short window consisting of the first few packets of a flow. 
FINC builds upon SetTree, a powerful tree-based model that supports variable-length inputs, and couple it with a stream-based data representation suited for real-time inference. Beyond per-packet features such as current inter-arrival time and length, FINC also supports aggregated statistical features such as \textit{mean} inter-arrival time and packet length, computed efficiently despite hardware limitations.

A new tree encoding and matching scheme is introduced to support deep trees while remaining within the SRAM and TCAM constraints of programmable switches. The system is implemented in P4 and evaluated on real IDS and DDoS datasets. The results show that our method achieves significantly higher accuracy than prior work using SRAM, and matches the accuracy of TCAM-based approaches while requiring much shallower trees and using a short window of only the first six packets of each flow.

<figure align="center">
  <img width="635" height="915" alt="FINC-Tree-Encoding" src="https://github.com/user-attachments/assets/38a3dd60-7349-4a62-a0f2-7e27880f213a" />
  <br>
  <figcaption><i>FINC-Tree-Encoding Scheme.</i></figcaption>
</figure>


## Requirements

## Using FINC

### P4 Parameters 
TBD

### Data Plane Compilation
TBD

### SetTree Training and Evaluation
TBD

### Datasets and Packet-level representation
TBD
