---
layout: post
title:  "Monitor System I/O"
categories: Mac system io file network
---

- lsof

		# e.g. check pid_1, pid_2, exclude pid_3 every second (-r 1)
		# for directory ~
		lsof -p pid_1,pid_2,^pid_3 -r 1 +d ~

		# e.g. check localhost TCP connection to ports 80~1024 and smtp
		lsof -i tcp@0:80-1024,smtp

		# e.g. check dev
		lsof /dev/disk5s1

- fs_usage

		sudo fs_usage pid

