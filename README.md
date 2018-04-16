# Cyber Labs

### Synopsis
This project provides a modularized lab setup that cybersecurity instructors can easily use to supplement their course materials. By completing these labs, students will gain significant exposure to critical cybersecurity tools.

### Introduction 

Traditional cybersecurity instruction at the undergraduate level relies overwhelmingly on theory as a method of conveying information. Students are often taught various networking and security concepts on a conceptual without actually getting a chance to interact with them. However, without hands-on experience with the tools to which these concepts apply, it may be more difficult for learners to effectively achieve a commanding grasp of the security concepts. Participative learning exercises and labs allow students to swiftly build mental bridges between seeming siloed concepts, and to confidently apply their knowledge in new scenarios. Such a skill makes students significantly more attractive in the job market as it reduces the burden on the employer as it relates to training. 

Perhaps one explanation for lack the of practical exercises in cybersecurity courses is the scarcity of easily accessible and applicable lab content. This void is especially present as it relates to introductory modules. In many situations, instructors neither have the time or expertise to create effective lab exercises nor the budget to purchase and install them in an environment accessible to students. 

This project attempts to create a modularized lab setup that cybersecurity instructors can easily use to supplement their course materials in introductory classes. It contains a series of gamified exercises centered around fundemental cybersecurity tools and concepts, all packaged neatly inside a virtual machine. Students may access the exercises by setting up the virtual machine locally or by connecting to networked instance of the virtual machine using the secure shell protocol (ssh).  This approach was inspired by the OverTheWire project: http://overthewire.org/ and by the Security Education (SEED) project.
	
### Structure

The exercises in this lab will be available through a series of folders on a virtual machine. Each folder will contain a README.md file with instructions containing the objectives for the lab. Based on the instructions in this file, students will use accessible tools to complete the objective for the round and obtain a passphrase which can be verified (either manually or automatically) by the instructor. In a basic exercise, for example, the student may use the “cat” command to read the content of a given file on the command line interface. He/she would use the acquired passphrase from the file to authenticate into the next exercise or take credit for accomplishing it. In a more advanced example, the student may be required to search within a network packet capture file for the passphrase being sent across the wire. 


### Software Requirements:

Virtualbox – This is virtualization product that allows users to manage multiple virtual machines. Virtualbox is freely for personal use and has extensive documentation for getting stated.  https://www.virtualbox.org/

Remux – This is a free linux toolkit for reverse engineering and malware analysis. This environment is preferred because it comes pre-installed with many tools students may need to complete the challenged. Alternatively, these exercises can be set up on a Kali linux of Sift virtual environment.  https://remnux.org/

### Content

1.	Virtual machine including all exercises
2.	Introduction to the Linux command line interface (CLI)
  * Presentation
  * Video demonstration
  * Lab instructions
  * Answer Key
3.	Text analysis using the CLI (grep, sed, awk)
  * Presentation
  * Video demonstration
  * Lab instructions
  * Answer key
4.	Analysis of phishing emails
  * Presentation
  * Video demonstration
  * Lab instructions
  * Answer key

