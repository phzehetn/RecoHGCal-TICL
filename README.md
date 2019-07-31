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
  - `v0`: Simple CNN. It does not yet contain the energy regression. The neutral hadron probability is set to a constant value of 0. See the [talk](https://indico.cern.ch/event/799486/contributions/3492052/subcontributions/284302/attachments/1875750/3088524/MLforTICL_Scrum.pdf) at the [Patatrack Hackathon](https://indico.cern.ch/event/799486) for more info. Input and output tensors:
    - `"input"`: Input tensor with dimension `batch x 50 (layers) x 10 (clusters) x 3 (features)`.
    - `"output/id_probabilities"`: Output tensor representing particle ID "probabilities" (from a softmax output) with dimension ` batch x 5`. The probabiltities refer to photon, electron, muon, charged hadron, neutral hadron (in that order).
