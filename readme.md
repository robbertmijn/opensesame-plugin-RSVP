# OpenSesame RSVP plug-in

## About

This plug-in allows you to add a Rapid Serial Visual Presentation element to your experiment.
The plug-in can be used, for example, in a concealed information test (CIT). The RSVP plug-in
allows for pupil size measurements during a CIT. Previous research has shown that pupil size 
cannot be actively manipulated, while CITs that measure other bodily sensations can be 
manipulated (Chen et al., 2021). 

The project included research into the implementation of pupil size measurements in CIT and
the development of open source tools (presenting stimuli (text/images) on the screen, 
preparation of the stimuli, and analysis of the data) to be used in CIT. The project is 
funded by Police & Science (Politie & Wetenschap). 

## Features
The RSVP plug-in provides an easy tool that can be implemented in an experiment. It contains
the following features:
* An automated rapid serial visual presentation;
* Compatible with both text and image stimuli;
* Contains an inter stimulus interval;
* Targets and distractors can shuffle;
* Number of targets and distractors can be adjusted;
* Position of the targets and distractors can be adjusted.

## Getting started
The plug-in works for OpenSesame, so make sure to have installed [OpenSesame](https://osdoc.cogsci.nl/3.2/download) on your computer.

Next, install the RSVP plug-in in OpenSesame as follows:
```
import pip
pip.main(['install', 'opensesame-plugin-rsvp'])
```

The plug-in should appear in the toolbar, under the category 'Visual stimuli'. 

## Usage

While building the experiment, one can drag the plug-in to the correct place in the trial
sequence.  Moreover, with inline scripts the variables like the targets and distractors can be
defined. In the experiment sequence, one should use an inline script to specify the targets 
and distractors. In the trial sequence, one should use an inline script to determine the 
stimuli that are presented in each trial. 

Based on the purpose of the experiment, one should change the mode to either text or image
stimuli. In addition, the corresponding files must be added to the **filepool**. 

For the targets and distractors, one can refer to specific files or previously defined 
variables. In addition, the filepool can contain a textfile with a list of filenames that are 
also in the filepool. This way, one can refer to multiple stimuli with a single file. The list 
of files in the textfile should be split by a new line (an enter, '/n'). Still, the files that 
are referred to in the textfile, should all be in the filepool.

When referring to multiple targets, distractors, or positions in the widget, these should be
split by a semicolon (';').

## License

No rights reserved. All files in this repository are released into the public domain.












