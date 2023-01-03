<!-- Improved compatibility of back to top link: See: https://github.com/othneildrew/Best-README-Template/pull/73 -->
<a name="readme-top"></a>
<!--
*** Thanks for checking out the Best-README-Template. If you have a suggestion
*** that would make this better, please fork the repo and create a pull request
*** or simply open an issue with the tag "enhancement".
*** Don't forget to give the project a star!
*** Thanks again! Now go create something AMAZING! :D
-->



<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->
[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]
[![LinkedIn][linkedin-shield]][linkedin-url]


<h3 align="center">Machine Learning Analysis of Structured Electronic Health Record Data</h3>

  <p align="center">
    Construction of various predictive models on a dataset of hospitalized heart failure patients
    <br />
    <a href="https://github.com/masadeghi/EHRsample"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <a href="https://github.com/masadeghi/EHRsample/issues">Report Bug</a>
    ·
    <a href="https://github.com/masadeghi/EHRsample/issues">Request Feature</a>
  </p>
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

In this project, I've applied machine learning methods to a dataset from hospitalized decompensated heart failure patients to construct predictive models. This dataset is provided by Zhang et al. on the PhysioNet website [1](https://physionet.org/content/heart-failure-zigong/1.3/#files) and contains 168 features for 2008 patients. An additional dataset contains all the medications administered to these patients during their hospital stay. Originally, the data was used to predict if patients would be readmitted to the emergency department within 6 months after discharge.

Here, I've used the data to predict the duration of hospital stay using features that are expected to be available shortly after patient admission (clinical presentation, lab tests, and drug order). For this task, I've used three distinct methods:

<ul>
  <li><b>linear_regression_svm_random_forest_sklearn.ipynb:</b> In this script, I've used non-neural network machine learning methods from scikit-learn, including regularized linear regressors, support vector machine regressors, random forest regressors, and a super ensemble of all these methods using a voting regressor.</li>
  <li><b>nn_pytorch.ipynb:</b> In this script, I've used a TabularModel neural network structure using PyTorch to perform the prediction.</li>
  <li><b>nn_tensorflow_with_model_optimization.ipynb:</b> In this script, I've used TensorFlow to build and optimize a neural network regressor. The optimization is performed in a step-by-step experimentation process and its results can be viewed using TensorBoard.</li>  
</ul>

References:

Zhang, Z., Cao, L., Zhao, Y., Xu, Z., Chen, R., Lv, L., & Xu, P. (2022). Hospitalized patients with heart failure: integrating electronic healthcare records and external outcome data (version 1.3). PhysioNet. https://doi.org/10.13026/5m60-vs44

Zhang Z, Cao L, Chen R, Zhao Y, Lv L, Xu Z, Xu P. Electronic healthcare records and external outcome data for hospitalized patients with heart failure. Sci Data. 2021 Feb 5;8(1):46. doi: 10.1038/s41597-021-00835-9. PMID: 33547290; PMCID: PMC7865067

<p align="right">(<a href="#readme-top">back to top</a>)</p>



### Built With

* Python v3.7.15

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- GETTING STARTED -->
## Getting Started

To access the data, you must sign up on the PhysioNet website and sign a Data Use Agreement to access the data files. After accessing the files, download the ZIP file.

### Installation

1. Upload the ZIP file to your Google Drive account.
2. Replace the paths in the following lines to reflect the file location in your Drive:
   ```sh
   drive.mount('/content/gdrive')
   ```
   ```sh
   !unzip gdrive/MyDrive/databases/hospitalized-patients-with-heart-failure-integrating-electronic-healthcare-records-and-external-outcome-data-1.3.zip
   ```
	 ```sh
	 patient_data = pd.read_csv('/content/hospitalized-patients-with-heart-failure-integrating-electronic-healthcare-records-and-external-outcome-data-1.3/dat.csv', index_col = 0)
	 
	 treatment_data = pd.read_csv('/content/hospitalized-patients-with-heart-failure-integrating-electronic-healthcare-records-and-external-outcome-data-1.3/dat_md.csv', index_col = 0)
	 
	 dict_data = pd.read_csv('/content/hospitalized-patients-with-heart-failure-integrating-electronic-healthcare-records-and-external-outcome-data-1.3/dataDictionary.csv', index_col = 0)
	 ```
3. Run the code. All dependencies (numpy, pandas, sklearn, seaborn) are preinstalled on Colab.

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- USAGE EXAMPLES -->
## Usage

This project is an example of applying linear, support vector machine, random forest, and voting (linear + svm + random forest) regressors to predict a quantitaive measure of value from biomedical data.

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE.txt` for more information.

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- CONTACT -->
## Contact

Amin Sadeghi - masadeghi6@gmail.com

Project Link: [https://github.com/masadeghi/EHRsample](https://github.com/masadeghi/EHRsample)

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/masadeghi/EHRsample.svg?style=for-the-badge
[contributors-url]: https://github.com/masadeghi/EHRsample/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/masadeghi/EHRsample.svg?style=for-the-badge
[forks-url]: https://github.com/masadeghi/EHRsample/network/members
[stars-shield]: https://img.shields.io/github/stars/masadeghi/EHRsample.svg?style=for-the-badge
[stars-url]: https://github.com/masadeghi/EHRsample/stargazers
[issues-shield]: https://img.shields.io/github/issues/masadeghi/EHRsample.svg?style=for-the-badge
[issues-url]: https://github.com/masadeghi/EHRsample/issues
[license-shield]: https://img.shields.io/github/license/masadeghi/EHRsample.svg?style=for-the-badge
[license-url]: https://github.com/masadeghi/EHRsample/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://www.linkedin.com/in/mohammad-amin-sadeghi-md/
