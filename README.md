# Data for the CMSSW [RecoHGCal/TICL](https://github.com/cms-sw/cmssw/tree/master/RecoHGCal/TICL) package

### Quicklinks

- TICL:
  - [Reconstruction example](http://hgcal.web.cern.ch/hgcal/Reconstruction/TICL/)
- TensorFlow:
  - [C++ docs](https://www.tensorflow.org/api_docs/cc)
  - [CMSSW interface](https://gitlab.cern.ch/mrieger/CMSSW-DNN)
  - [PhysicsTools/TensorFlow](https://github.com/cms-sw/cmssw/tree/master/PhysicsTools/TensorFlow)

### Models

- `tf_models/energy_id_cnn_v*.pb`: TensorFlow model for trackster energy regression and ID.
  - `v0`: Simple CNN. It does not yet contain the energy regression. [Talk](https://indico.cern.ch/event/799486/contributions/3492052/subcontributions/284302/attachments/1875750/3088524/MLforTICL_Scrum.pdf) at the [Patatrack Hackathon](https://indico.cern.ch/event/799486).
