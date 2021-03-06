.. LFPy documentation master file, created by
    sphinx-quickstart on Mon Oct  3 13:36:41 2011.
    You can adapt this file completely to your liking, but it should at least
    contain the root `toctree` directive.

.. image:: Logo_liten.png

LFPy Homepage
=============

(Looking for the old LFPy documentation? Follow `link <https://lfpy.github.io/v1.3>`_)

LFPy is a `Python <http://www.python.org>`_ package for calculation of extracellular potentials from multicompartment neuron models and recurrent networks of multicompartment neurons.
It relies on the `NEURON simulator <http://www.neuron.yale.edu/neuron/>`_ and uses the
`Python interface <http://www.frontiersin.org/neuroinformatics/10.3389/neuro.11.001.2009/abstract>`_ it provides.

Active development of LFPy, as well as issue tracking and revision tracking, relies on `GitHub.com <https://github.com/LFPy/LFPy>`_ and `git (git-scm.com) <https://git-scm.com>`_.
Clone LFPy on `GitHub.com <https://github.com/LFPy/LFPy>`_: ``git clone https://github.com/LFPy/LFPy.git``

LFPy provides a set of easy-to-use Python classes for setting up your model, running your simulations and calculating the extracellular potentials arising from activity in your model neuron. If you have a model
working in `NEURON <http://www.neuron.yale.edu>`_ or `NeuroML2 <https://www.neuroml.org/neuromlv2>`_
already, it is likely that it can be adapted to work with LFPy.

The extracellular potentials are calculated from transmembrane currents in multi-compartment neuron models using the line-source method (Holt & Koch, J Comp Neurosci 1999),
but a simpler point-source method is also available. The calculations assume that the neuron are surrounded by an infinite extracellular medium with homogeneous and
frequency independent conductivity, and compartments are assumed to be at least at a minimal distance from the electrode (which can be specified by the user).
For more information on the biophysics underlying the numerical framework used see this coming book chapter:

- K.H. Pettersen, H. Linden, A.M. Dale and G.T. Einevoll: Extracellular spikes and current-source density, in *Handbook of Neural Activity Measurement*,
  edited by R. Brette and A. Destexhe, Cambridge, to appear `[preprint PDF, 5.7MB] <http://www.csc.kth.se/~helinden/PettersenLindenDaleEinevoll-BookChapter-revised.pdf>`_

In previous versions (v1.x.x), LFPy was mainly designed for simulation of single neurons,
but the forward modeling scheme is in general applicable to neuronal populations.
These aspects, and the biophysical assumptions behind LFPy is described in our paper on the package appearing in Frontiers in Neuroinformatics, entitled `"LFPy: A tool for biophysical simulation of extracellular potentials generated by detailed model neurons" <http://dx.doi.org/10.3389%2Ffninf.2013.00041>`_,
appearing as part of the research topic `"Python in Neuroscience II" <http://www.frontiersin.org/Neuroinformatics/researchtopics/Python_in_Neuroscience_II/1591/>`_.

Since v2, LFPy also supports networks of multicompartment neurons, calculations of current-dipole moments, and predictions of both electric potentials and magnetic signals from a series of different volume-conductor models, as described in
the bioRXiv preprint "Multimodal modeling of neural network activity: computing LFP, ECoG, EEG and MEG signals with LFPy2.0" by Espen Hagen, Solveig Næss, Torbjørn V Ness, Gaute T Einevoll, found at `https://doi.org/10.1101/281717 <https://doi.org/10.1101/281717>`_.

Citations:

- LFPy v2.x: Hagen E, Næss S, Ness TV and Einevoll GT (2018) Multimodal Modeling of Neural Network Activity: Computing LFP, ECoG, EEG, and MEG Signals With LFPy 2.0. Front. Neuroinform. 12:92. doi: 10.3389/fninf.2018.00092. https://dx.doi.org/10.3389/fninf.2018.00092
- LFPy v1.x: Linden H, Hagen E, Leski S, Norheim ES, Pettersen KH and Einevoll GT (2013). LFPy: A tool for biophysical simulation of extracellular potentials generated by detailed model neurons. Front. Neuroinform. 7:41. doi: 10.3389/fninf.2013.00041. https://dx.doi.org/10.3389/fninf.2013.00041


LFPy was developed in the `Computational Neuroscience Group`, `Department of Mathemathical Sciences and Technology <http://www.nmbu.no/imt>`_,
at the `Norwegian University of Life Sciences <http://www.nmbu.no>`_ ,
in collaboration with the `Laboratory of Neuroinformatics <http://www.nencki.gov.pl/en/laboratory-of-neuroinformatics>`_,
`Nencki Institute of Experimental Biology <http://www.nencki.gov.pl>`_, Warsaw, Poland,
and `Center for Integrative Neuroplasticity (CINPLA) <http://cinpla.org>`_ at the University of Oslo, Norway.
The effort was supported by
`International Neuroinformatics Coordinating Facility <http://incf.org>`_ (`INCF <http://incf.org>`_), `The Research Council of Norway <http://www.forskningsradet.no/english/>`_ (eScience, NevroNor, COBRA) and `EU-FP7 (BrainScaleS) <http://www.brainscales.org>`_.

This scientific software is released under the GNU Public License `GPLv3 <http://www.gnu.org/copyleft/gpl.html>`_.

Tutorial slides on LFPy
-----------------------

Slides for OCNS 2018 meeting tutorial `T5: Modeling and analysis of extracellular potentials <https://www.cnsorg.org/cns-2018-tutorials#T5>`_ hosted in Seattle, USA on LFPy: `CNS2018_LFPy_tutorial.pdf  <http://LFPy.github.io/downloads/CNS2018_LFPy_tutorial.pdf>`_

Slides for OCNS 2017 meeting tutorial `T4: Modeling and analysis of extracellular potentials <http://www.cnsorg.org/cns-2017-tutorials#t4>`_ hosted in Antwerp, Belgium on LFPy and hybridLFPy: `CNS2017_LFPy_tutorial.pdf  <http://LFPy.github.io/downloads/CNS2017_LFPy_tutorial.pdf>`_

Slides from OCNS 2015 meeting tutorial `T2:  Modeling and analysis of extracellular potentials <http://www.cnsorg.org/cns-2015-tutorials#t2>`_ hosted in Prague, Czech Republic on LFPy and hybridLFPy: `CNS2015_LFPy_tutorial.pdf  <http://LFPy.github.io/downloads/CNS2015_LFPy_tutorial.pdf>`_

Slides from OCNS 2014 meeting tutorial `T4:  Modeling and analysis of extracellular potentials <http://www.cnsorg.org/cns-2014-tutorials#T4>`_ hosted in Quebec City: `hybridlfpy_tutorial_OCNS2014.pdf  <http://LFPy.github.io/downloads/hybridlfpy_tutorial_OCNS2014.pdf>`_

As part of the OCNS 2013 meeting workshop `Modeling and interpretation of extracellular potentials <http://www.cnsorg.org/cns-2013-tutorials#extracellular_potentials>`_,
there was also a talk on LFPy.
The slides can be found here: `lfpy-tutorial_OCNS2013.pdf  <http://LFPy.github.io/downloads/lfpy-tutorial_OCNS2013.pdf>`_.


Related projects
----------------

LFPy has been used extensively in ongoing and published work, and may be a required dependency by the publicly available Python modules:

- ViSAPy - Virtual Spiking Activity in Python (https://github.com/espenhgn/ViSAPy, http://software.incf.org/software/visapy),
  as described in Hagen, E., et al. (2015), J Neurosci Meth, DOI:`10.1016/j.jneumeth.2015.01.029 <http://dx.doi.org/10.1016/j.jneumeth.2015.01.029>`_
- ViMEAPy that can be used to incorporate heterogeneous conductivity in calculations of extracellular potentials with LFPy
  (https://bitbucket.org/torbness/vimeapy, http://software.incf.org/software/vimeapy). ViMEAPy and it's application is described
  in Ness, T. V., et al. (2015), Neuroinform, DOI:`10.1007/s12021-015-9265-6 <http://dx.doi.org/10.1007/s12021-015-9265-6>`_.
- hybridLFPy - biophysics-based hybrid scheme for calculating the local field potential (LFP) of spiking activity in simplified
  point-neuron network models (https://github.com/INM-6/hybridLFPy),
  as described in Hagen, E. and Dahmen, D., et al. (2016), Cereb Cortex, DOI:`10.1093/cercor/bhw237 <http://dx.doi.org/10.1093/cercor/bhw237>`_




Contents
========
.. toctree::
    :maxdepth: 3

    information
    tutorial
    additional
    classes

Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`
