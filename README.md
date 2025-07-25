# Docker for BepiPred-3.0 software

More information:  
[https://services.healthtech.dtu.dk/services/BepiPred-3.0/](https://services.healthtech.dtu.dk/services/BepiPred-3.0/)

## 🔧 Build Image

```bash
sudo docker build -t bepipred:3 -f Dockerfile .
```

## 🚀 Run with GPU

```bash
sudo docker run --rm -it --gpus all -v ${PWD}:/data/ bepipred:3 -i /example_antigens.fasta -pred vt_pred -o /data/test/gpu
```

## ⚙️ Run with CPU

```bash
sudo docker run --rm -it -v ${PWD}:/data/ bepipred:3 -i /example_antigens.fasta -pred vt_pred -o /data/test/cpu
```

## 📚 Please cite:

- Clifford, J. N., Høie, M. H., Deleuran, S., Peters, B., Nielsen, M., & Marcatili, P. (2022). BepiPred-3.0: Improved B-cell epitope prediction using protein language models. Protein science : a publication of the Protein Society, 31(12), e4497. https://doi.org/10.1002/pro.4497

- Moreira, R. S., Filho, V. B., Calomeno, N. A., Wagner, G., & Miletti, L. C. (2022). EpiBuilder: A Tool for Assembling, Searching, and Classifying B-Cell Epitopes. Bioinformatics and biology insights, 16, 11779322221095221. https://doi.org/10.1177/11779322221095221
