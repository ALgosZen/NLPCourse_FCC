Troubleshooting NLP in Jupiter notebook
>>’No module named spacy' in ipython, but works fine in regular python interpretter
>>alternative without installing Jupyter inside your venv is:
$ python -m venv NLPProject
$ source NLPProject/bin/activate
(venv) $ pip install ipykernel
(venv) $ ipython kernel install --user --name=NLPProject
(venv) $ conda install -c conda-forge spacy (or use pip as you would)
(venv) $ jupyter notebook
—
Make sure you select new kernel (load project kernel in Jupyter)

————
In case you are using pip and If pip is not recognized in jupyter
alias pip=/usr/local/bin/pip3
Or 
Alias pip=/opt/homebrew/bin/pip3

——
Setting python 3 as default  (Montery OS has both installed but python 2 is default as usual)

Pytho —version (double hyphen)
Python3 —version
sudo ln -s -f /opt/homebrew/bin/python3 /usr/local/bin/python

—
Install spacy and download trained pipeline in English
pip install -U 'spacy[apple]'
python -m spacy download en_core_web_sm
—

