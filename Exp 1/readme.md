Experiment 1: Forensic Evidence Acquisition and Hashing

Objective
The goal of this experiment was to capture a complete physical clone of a storage medium and validate its authenticity through SHA-256 hashing, ensuring the data remains identical to the original source.

Tools Utilized

FTK Imager v4.5
HashCalc (employed for redundant hash validation)
Procedural Overview
The process began by connecting a 4GB USB flash drive to serve as the primary evidence. Using FTK Imager, a physical image was generated in the E01 (EnCase) format. The acquisition settings included a compression level of 6 and the activation of automated hash verification. A SHA-256 hash was produced during this stage to serve as a unique digital signature for the drive.

Results
The imaging process was completed without errors. The resulting hash value was identical to the source drive's hash, demonstrating that the bit-stream acquisition was accurate and the evidence integrity was maintained.
