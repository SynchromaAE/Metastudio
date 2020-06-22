The Metastudio is a collection of sequencing, synthesis, processing and production tools for Pure Data.
It uses Pd-extended-0.41.4 which can be downloaded from:
 
http://puredata.info



IMPORTANT!
You must put the metastudio-0.5 folder into your path either by adding it from the file -> path... (or on Mac, Preferences -> Path) dialogue in Pd, or by loading Pd with the flag -path /path/to/metastudio-0.5 in order for the abstractions to work properly.



Check the app/ folder for complete applications of the metastudio, but keep an eye on the website for updates.
This archive is regularly updated with bugfixes, help patches and new objects. 
You can download it from:
 
http://sharktracks.co.uk/puredata


Enjoy!



----------Version History--------
version 0.5 - many more help files!
New objects: stwang~


version 0.3.13 - isoseq now has reframing within the length of the sequence, separate for durations and values. clinoker~ and clinok~ can now be used with phasevocoder~ as the filters are directly referenced to cyclone/svf~ rather than bsaylor/svf~ (bsaylor version has denormal errors!!!). Help file for trigseq64. trigseq64 can now load earlier trigseq patterns (trigseq, and seq-5t-32 from metastudio 0.2). New modular synth units - trapeze~ oscillator and vcfvcaeg~ amp and filter envelopes. Fixed and rationalized Analogy_Drums.pd in app/ folder. New machines - stwang~ sample+FM, damped~ resonated impulse, stereo_drift~ delay/comb flanger.

version 0.3.12 - MIDI step entry for sequencers. Separate playchunks_1~ (_2~, _3~, _4~) and new GUI. Trigseq64 and sequencer64 - reframing in trigseq64.



version 0.3.10

 - nicer knobs for knobs! mix12~ has new methods - e.g. randvol.
 - fixed the sequencer preset pattern so the help file works! New preset file for fmf_perc~ (help file on the way soon).



version 0.3-09

 - new help file for mix12~
 - fixed phasevocoder~ so that loop start/end points update on each loop cycle.



version 0.3-08

 - fixed a big bug with the sequencer!!!! New pattern should work as expected now, but you may not be able to load old patterns. Next release should include a line-checker, so that patterns with old formats (lengths) from earlier metastudio 3 and metastudio 2 releases can be loaded.



version 0.3-07

 - added nogui versions of MIDI value converters midi_tc (m_tc), midi_pcf (m_pcf), midi_pc (m_pc), midi_pf (m_pf), midi_fcq (m_fcq) and midi_fc (m_fc).
 - rolled back filter in clinoker~ and clinok~ to svf~ rather than bsaylor/svf~. There are problems with bsaylor/svf~ pegging the CPU due to denormals. Research into fixing bsaylor's version is ongoing!
 - removed svf_fl~.pd since this conflicts with the old svf~ (see above). DO NOT USE bsaylor/svf~ since it will cause pd to load the wrong filter.
 - 'salted' the freeverber~ with noise to overcome denormals, and the moog_fl~ plugin (but this one might not work! denormals still seem to happen).



version 0.3-06

 - fixed the midi_spiral object so that instead of using the math to create the tables and to alter the midi data, now the midi input only accesses the tables (much faster / more stable).
 - fixed a bug in the phasevocoder~ object so that loops are now working!



version 0.3-05

 - fixed a bug in the clinoker~ object that caused the noise section to not work
 - enabled list input to midi_spiral, help patch coming soon...



version 0.3-04

 - finished the help patch for trigseq.pd



version 0.3-03

 - added examples to help-trigseq.pd
 - fixed the phasynth~ abstraction



version 0.3-02

 - fixed a bug in trigseq, which meant that Windows users could not save sequence files



version 0.3-01

 - added [done( message to right outlet of sampleboxes, so that the patch outputs a bang 100ms after all samples are loaded.



version 0.3

 - initial release, Sao Paulo, Brasil, July 21st 2009



version 0.2, 0.1

 - first version of metastudio (2007) had no help patches and was difficult to use! Inconsistent external accessing of parameters and some cumbersome routing issues.



-------------------TODO----------------------

 

- more help files

- a better mechanism for swapping synchronisation sources
 

- modpatch is still flakey - to be fixed soon
 

- implement iemguts-based configuration for sampler_matrix~.pd (when it is part of Pd-extended)

- fix seq_events to be smaller and more rational

- and more...a master sequencing patch, perhaps based on modpatch.
