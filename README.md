# Home-Appliance-Control-Dataset
A Comprehensive Dataset for Home Appliance Control using ERP-Based BCIs

![figure2](https://github.com/jml226/Home-Appliance-Control-Dataset/assets/128969655/4d415a6a-180f-40a8-a8cb-c0936b5506d1)

 All the BCI experiments for home appliance control shared an identical experimental procedure. The experiments consisted of a series of blocks of the oddball task (Figure A). A single block began with 0.5-second fixation where a white cross appeared at the center of the screen. The preview of stimuli followed for 1 second which allowed subjects to perceive all the stimuli. Then, a target stimulus was instructed by changing the color of the border of the target stimulus to red for 1 second. Each stimulus flickered in a random order, which took 5 seconds total. Afterward, the feedback of BCI control was shown for 1 second, and subjects rested for 2 seconds until the next block. During the training phase, 50 blocks were repeated, while in the testing phase, 30 blocks were repeated. Specific paradigms for each home appliance are described below (see also Figures B to F.)

 To develop a BCI for controlling TV channels, an emulated Multiview TV platform was created. This platform displayed four preview channels simultaneously at four quadrants from the center of the screen (Figure B). The video clips in each channel served as both channel previews and visual distractors. The video clips were presented on a 50-inch Ultra High Definition (UHD) TV with a resolution of 1920 × 1080 and a refresh rate of 60 Hz. Additional red stimuli flickering at a frequency of 8 Hz surrounded the corners of the video clip windows. Each block began with the subject fixating their gaze at the center of the screen, followed by an instruction indicating the target channel by turning its boundary red. Subsequently, the four video clips and their surrounding stimuli were displayed, each flickering ten times in a random order. Subjects were instructed to gaze at the stimulus surrounding the target channel while seated comfortably 2.5 meters away from the TV screen. The video clip of the selected channel was then displayed for 1 second as feedback.
The BCI experiments for controlling door locks (DL) and electric lights (EL) presented the stimuli on a tablet PC screen (Figures 2C and 2D). Subjects were instructed to select one of the two control icons for door lock control (lock/unlock) or one of three icons for electric light control (on/off/dim). To maintain a target-to-non-target stimulus ratio of 1:3 (4 classes), dummy stimuli were added to the task. Although the number of commands for TV, EL, and DL varied, dummy stimuli were added to ensure that the classifier could differentiate among four targets (target-to-non-target stimulus ratio of 1:3). Additionally, a shared characteristic among all three experiments was the utilization of an LCD environment for stimulus presentation. Consequently, these experiments were categorized under a unified paradigm referred to as the 4-class LCD paradigm. The BCI experiment to control Bluetooth speakers (BS) was conducted in which subjects selected one of the six functions (on/ off/ play/ pause/ next track/ previous track). In this experiment, the target-to-non-target stimulus ratio was maintained at 1:5 (Figure E). A BCI experiment was conducted to control air conditioners (AC) through an AR environment. The AR stimuli were displayed on Microsoft's HoloLens 1, which had a resolution 2 HD 16:9 light engines - 2.3 million light points. The BCI for AC control consisted of four functions (on/ off/ + temperature/ - temperature). The target-to-non-target stimulus ratio was maintained at 1:3 (Figure F). 
The stimuli were presented in the form of icons representing control functions in the four experiments (DL, EL, BS and AC). All the stimuli were displayed in blue. Then, during the stimulus flickering period, each stimulus flickered in a random order by briefly changing its color to light green for 0.625 seconds. The inter-stimulus interval was 0.125 second. Each stimulus flickered 10 times in the stimulus flickering period (McFarland et al., 2011). The home appliances to be controlled were displayed in the background of the screen in the DL, El and AC experiments, while no display of the device was provided in the BS experiment (Figure).

 The data acquired from the experiments had a hierarchical structure, comprising three levels. A summary of the dataset information is provided in Table 1. First Level: Home Appliance Type. The first level categorized the data based on the type of home appliance being controlled through the BCI. Second Level: Subject. Within each home appliance category, the data was further divided based on the subject. Each subject was anonymized and identified only by a unique ID. Third Level: Block-Specific Data. The third level contained the granular, block-based data for each subject. The data files were named following a specific convention for easy identification: SubX_training refers to the training data for subject X, and SubX_test_tr_Y refers to the test data for the Y-th block of subject X. Each data file at the third level was composed of two main components:

-Data.signal: it contains EEG signals in a matrix format, with dimensions; [channel x time (points)].

-Data.trigger: it contains the event trigger data in a row vector format, with dimensions; [1 x time (points)].

The trigger types are coded as follows:

-11: Block start

-12: Stimulation start

-13: Block end

-1 to 6: Types of stimuli

-Between 11 and 12: Indicates the target stimulus.


