# Table of Contents
1. [Overview](#overview)
2. [Setup](#setup)

  a). [Puppetfile](#puppetfile)
  
3. [Usage](#usage)

## Overview
R10k is a tool to deploy Puppet environments and modules with granular precision. It utilizes a Puppetfile format along with dynamic branch => environment mapping. This is an old control repo tested during a previous position.

Specs:
+ Supports Ruby versions **1.9.3 (in use)**, 2.0.0, 2.1.0.
+ R10k version 2.3.0
+ Puppet version > 3.0.0
+ Git/SVN required

## Setup
### Puppetfile
A Puppetfile is a Ruby based DSL that lists modules to install, what version to install, where to pull the modules from, and where to install them. 

The current implmentation of the Puppetfile in r10k does **not include dependency resolution** but it is currently in development. 

#### Commands
Librarian puppet and r10k have a select list of commands pertaining solely to the Puppetfile. These commands assume that the Puppetfile to operate on is in the current working directory, and modules specified should be installed in the 'modules' directory relative to the current working directory. 

1. Update and/or install all modulesi n a given Puppetfile

  `r10k puppetfile install`
2. Check Puppetfile syntax 

  `r10k puppetfile check`
3. Remove modules not specified in Puppetfile 

  `r10k puppetfile purge`

#### Syntax
##### forge
At the top of the Puppetfile, the `forge` setting tells r10k which server the Forge modules are pulled from. 

## Usage
