# neutron-net
![neutron-curve](/resources/figures/real/Figure%203.png) <br/>
A lightweight tool to analyse neutron reflectivity curves and generate initial refnx fits.

## About the Project
This repository contains the [code](/neutron-net) for a neural network-based pipeline for the automatic estimation of thin film thicknesses and scattering length densities from neutron reflectivity curves of systems containing up to three layers on top of a substrate. Raw instrument data (in our case from the OFFSPEC neutron reflectometer) is processed and passed through the pipeline to produce layer parameter predictions. These predictions are then fed into refnx, and serve as initial "guesses" for further optimisation to yield a model that likely describes a given sample. All that is required from the end user is running the [pipeline.py](/neutron-net/pipeline.py) file with their reflectivity data.

The project was motivated by the desire to enable on-experiment analysis of reflectivity data, informing choices about changing experiment conditions or samples <em>in operando</em>. 

### Citation
Please cite the following article if you intend on including elements of this work in your own publications:
> Mironov, D., Durant, J. H., Mackenzie, R. and Cooper, J. F. K. Towards automated analysis for neutron reflectivity. _Mach. Learn.: Sci. Technol._ **2**, 035006 (2021).

Or with BibTeX as:
```
@article{Mironov2021,
  author    = {Mironov, D. and Durant, J. H. and Mackenzie, R. and Cooper, J. F. K.},
  doi       = {10.1088/2632-2153/abe7b5},
  journal   = {Machine Learning: Science and Technology},
  month     = {Apr},
  number    = {3},
  pages     = {035006},
  publisher = {{IOP} Publishing},
  title     = {Towards automated analysis for neutron reflectivity},
  url       = {https://doi.org/10.1088/2632-2153/abe7b5},
  volume    = {2},
  year      = {2021}
}
```

## Installation
1. To replicate the development environment with the [`Anaconda`](https://www.anaconda.com/products/individual) distribution, first create an empty conda environment by running: `conda create --name neutron-net`

2. To activate the environment, run: `conda activate neutron-net`

3. Install pip by running: `conda install pip`

4. Navigate to the main neutron-net directory. Run the following to install the required packages from the [requirements.txt](/requirements.txt) file: `pip install -r requirements.txt`

5. You should be able to run the code. Try: `python pipeline.py`

## Usage
Please read [usage](/usage.md) for detailed instructions on how to use the system.

## Figures and Data
Additional figures to those seen in the article are available [here](/resources/figures) and training losses for the neutron and x-ray models are available [here](/resources/training). 

The synthetic data used for training the [neutron](/neutron-net/models/neutron) and [x-ray](/neutron-net/models/xray) models is available for download [`here`](https://drive.google.com/drive/folders/1meHjrb2812QSvZPaBXc7i02fbsu4AH6Y?usp=sharing).

## Contact
Jos Cooper - jos.cooper@stfc.ac.uk \
James Durant - james.durant@warwick.ac.uk \
Daniil Mironov - daniil.mironov@stfc.ac.uk

## Acknowledgements
Many thanks for the collaboration of the Scientific Machine Learning group at the Rutherford Appleton Laboratory, their expertise and assistance with this project - in particular, we'd like to thank Rebecca Mackenzie for being so key in laying the groundwork, and giving the project a strong foundation. The authors would like to thank Johnathan Xue, whose initial work and results allowed the project to go ahead. We thank the Ada Lovelace Centre for funding.

This work was partially supported by Wave 1 of The UKRI Strategic Priorities Fund under the EPSRC Grant EP/T001569/1, particularly the “AI for Science” theme within that grant & The Alan Turing Institute.

## Contributing
Contributions are gladly accepted and would be very much appreciated.

  1. Fork the project
  2. Create your feature branch (```git checkout -b feature/AmazingFeature```)
  3. Commit your changes (```git commit -m 'Add some AmazingFeature'```)
  4. Push to the branch (```git push origin feature/AmazingFeature```)
  5. Open a pull request

## License
Distributed under the GNU AGPLv3 license. See [license](/LICENSE) for more information.
