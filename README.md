Docker for BepiPred-3.0 software

More information https://services.healthtech.dtu.dk/services/BepiPred-3.0/

#Build Image
sudo docker build -t bepipred:3 -f Dockerfile .

#GPU
sudo docker run --rm -it --gpus all -v ${PWD}:/data/ bepipred:3 -i /example_antigens.fasta -pred vt_pred -o /data/test/gpu

#CPU
sudo docker run --rm -it -v ${PWD}:/data/ bepipred:3 -i /example_antigens.fasta -pred vt_pred -o /data/test/cpu
