# OpenSesame RSVP plug-in

![RSVP_plugin](/opensesame_plugins/RSVP_plugin/RSVP_plugin_large.png)

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

Next, install the RSVP plug-in in the console of OpenSesame as follows:
```
import pip
pip.main(['install', 'opensesame-plugin-rsvp'])
```

The plug-in should appear in the toolbar, under the category 'Visual stimuli'. 

<img width="356" alt="OS_plugin_image" src="https://user-images.githubusercontent.com/99414733/173846109-1f5c93a3-07ab-4c86-a0e1-96cd4f6ded25.png">

## Usage

The plugin looks as follows:

![GUI](/GUI.png)

The plugin shows several elements that can be adjusted to one's wishes. The following elements
can be adjusted:
* mode (text or images)
* targets
* number of targets
* shuffle targets
* distractors
* number of distractors
* shuffle distractors
* stimulus duration
* fixation duration
* positions of the targets
* inter stimulus interval

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

#### Text stimuli
If the stimuli are **text**, one can type in the target text in the widget, separated by a 
semicolon (';').Another option is to make a textfile ('.txt') with a list of all target words, 
separated by a new line ('/n'). This textfile should be added to the **filepool**, and the 
name of this textfile can be filled in in the widget. For example, the file can be named 
'targets.txt' and this should be filled in in the widget, of course without the quotes. The same 
goes for the distractors.

#### Image stimuli
If the stimuli are **images**, one should **always add all images** of the experiment to the 
**filepool**. In addition, a textfile can be created with a list of all targets. This textfile 
contains all filenames of the images and these files are separated by an enter. The textfile is 
also added to the filepool and can be referred to in the widget, instead of listing all files 
separated by a semicolon. This is the same for the distractors.

## License

No rights reserved. All files in this repository are released into the public domain.


