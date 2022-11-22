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
    <a href="https://github.com/masadeghi/EHRsample">View Demo</a>
    ·
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

In this project, I've applied machine learning methods to construct predictive models from a dataset on heart failure patients. This dataset is provided by Zhang et al. on the PhysioNet website [1](https://physionet.org/content/heart-failure-zigong/1.3/#files), and contains 168 variables for 2,008 patients with heart failure. An additional dataset contains all the medications administered to the patients during their hospital stay. Originally, the data was used to predict emergency readmission of discharged patients.

Here, I've used the data for the following tasks:
<ul>
  <li>Predicting the duration of hospitalization using data that is expected to be available shortly after patient admission (Patient history, physical exam, lab tests, and drug order)</li>
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
	 heart_data = pd.read_csv('/content/hospitalized-patients-with-heart-failure-integrating-electronic-healthcare-records-and-external-outcome-data-1.3/dat.csv')
	 
	 md_data = pd.read_csv('/content/hospitalized-patients-with-heart-failure-integrating-electronic-healthcare-records-and-external-outcome-data-1.3/dat_md.csv')
	 
	 dict_data = pd.read_csv('/content/hospitalized-patients-with-heart-failure-integrating-electronic-healthcare-records-and-external-outcome-data-1.3/dataDictionary.csv')
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
[stars-url]: https://github.com/masadeghi/repo_name/stargazers
[issues-shield]: https://img.shields.io/github/issues/masadeghi/EHRsample.svg?style=for-the-badge
[issues-url]: https://github.com/masadeghi/EHRsample/issues
[license-shield]: https://img.shields.io/github/license/masadeghi/EHRsample.svg?style=for-the-badge
[license-url]: https://github.com/masadeghi/EHRsample/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://www.linkedin.com/in/mohammad-amin-sadeghi-md/
