```
(base) mariospattichis@Marioss-MacBook-Pro-802 python % git clone https://github.com/ageron/handson-mlp.git
Cloning into 'handson-mlp'...
remote: Enumerating objects: 132, done.
remote: Counting objects: 100% (55/55), done.
remote: Compressing objects: 100% (39/39), done.
remote: Total 132 (delta 25), reused 36 (delta 16), pack-reused 77 (from 1)
Receiving objects: 100% (132/132), 33.35 MiB | 10.41 MiB/s, done.
Resolving deltas: 100% (41/41), done.
(base) mariospattichis@Marioss-MacBook-Pro-802 python % cd handson-mlp
(base) mariospattichis@Marioss-MacBook-Pro-802 handson-mlp % pwd
/Users/mariospattichis/Dropbox/new-classes/python/handson-mlp
(base) mariospattichis@Marioss-MacBook-Pro-802 handson-mlp % conda update -n base -c defaults conda
Retrieving notices: ...working... done
Channels:
 - defaults
 - cogsci
Platform: osx-arm64
Collecting package metadata (repodata.json): done
Solving environment: done

## Package Plan ##

  environment location: /Users/mariospattichis/anaconda3

  added / updated specs:
    - conda


The following packages will be downloaded:

    package                    |            build
    ---------------------------|-----------------
    ca-certificates-2025.7.15  |       hca03da5_0         127 KB
    certifi-2025.8.3           |  py312hca03da5_0         161 KB
    conda-24.11.3              |  py312hca03da5_0         1.2 MB
    openssl-3.0.17             |       h4ee41c1_0         4.3 MB
    ------------------------------------------------------------
                                           Total:         5.7 MB

The following packages will be UPDATED:

  ca-certificates                      2024.9.24-hca03da5_0 --> 2025.7.15-hca03da5_0 
  certifi                         2024.8.30-py312hca03da5_0 --> 2025.8.3-py312hca03da5_0 
  conda                              24.9.2-py312hca03da5_0 --> 24.11.3-py312hca03da5_0 
  openssl                                 3.0.15-h80987f9_0 --> 3.0.17-h4ee41c1_0 


Proceed ([y]/n)? 


Downloading and Extracting Packages:
                                                                                                                                                            
Preparing transaction: done                                                                                                                                 
Verifying transaction: done                                                                                                                                 
Executing transaction: done                                                                                                                                 
(base) mariospattichis@Marioss-MacBook-Pro-802 handson-mlp % vim environment.yml                
(base) mariospattichis@Marioss-MacBook-Pro-802 handson-mlp % conda env create -f environment.yml
Channels:
 - conda-forge
Platform: osx-arm64
Collecting package metadata (repodata.json): done
Solving environment: done

Downloading and Extracting Packages:
                                                                                                                          
Preparing transaction: done                                                                                               
Verifying transaction: done                                                                                               
Executing transaction: /                                                                                                  
\                                                                                                                         
/                                                                                                                         
done                                                                                                                      
Installing pip dependencies: / Ran pip subprocess with arguments:                                                         
['/Users/mariospattichis/anaconda3/envs/homlp/bin/python', '-m', 'pip', 'install', '-U', '-r', '/Users/mariospattichis/Library/CloudStorage/Dropbox/new-classes/python/handson-mlp/condaenv.zasdf3a6.requirements.txt', '--exists-action=b']        
Pip subprocess output:                                                                                                    
Collecting AutoROM (from -r /Users/mariospattichis/Library/CloudStorage/Dropbox/new-classes/python/handson-mlp/condaenv.zasdf3a6.requirements.txt (line 1))                                                                                         
  Downloading AutoROM-0.6.1-py3-none-any.whl.metadata (2.4 kB)                                                            
Collecting torch-tb-profiler (from -r /Users/mariospattichis/Library/CloudStorage/Dropbox/new-classes/python/handson-mlp/condaenv.zasdf3a6.requirements.txt (line 2))                                                                               
  Downloading torch_tb_profiler-0.4.3-py3-none-any.whl.metadata (1.4 kB)                                                  
Collecting urlextract (from -r /Users/mariospattichis/Library/CloudStorage/Dropbox/new-classes/python/handson-mlp/condaenv.zasdf3a6.requirements.txt (line 3))                                                                                      
  Downloading urlextract-1.9.0-py3-none-any.whl.metadata (5.8 kB)                                                         
Collecting bitsandbytes (from -r /Users/mariospattichis/Library/CloudStorage/Dropbox/new-classes/python/handson-mlp/condaenv.zasdf3a6.requirements.txt (line 4))                                                                                    
  Downloading bitsandbytes-0.42.0-py3-none-any.whl.metadata (9.9 kB)                                                      
Requirement already satisfied: hf_xet in /Users/mariospattichis/anaconda3/envs/homlp/lib/python3.12/site-packages (from -r /Users/mariospattichis/Library/CloudStorage/Dropbox/new-classes/python/handson-mlp/condaenv.zasdf3a6.requirements.txt (line 5)) (1.1.8)                                                                                                            
Collecting lap (from -r /Users/mariospattichis/Library/CloudStorage/Dropbox/new-classes/python/handson-mlp/condaenv.zasdf3a6.requirements.txt (line 6))                                                                                             
  Downloading lap-0.5.12-cp312-cp312-macosx_11_0_arm64.whl.metadata (6.2 kB)                                              
Requirement already satisfied: click in /Users/mariospattichis/anaconda3/envs/homlp/lib/python3.12/site-packages (from AutoROM->-r /Users/mariospattichis/Library/CloudStorage/Dropbox/new-classes/python/handson-mlp/condaenv.zasdf3a6.requirements.txt (line 1)) (8.2.1)                                                                                                    
Requirement already satisfied: requests in /Users/mariospattichis/anaconda3/envs/homlp/lib/python3.12/site-packages (from AutoROM->-r /Users/mariospattichis/Library/CloudStorage/Dropbox/new-classes/python/handson-mlp/condaenv.zasdf3a6.requirements.txt (line 1)) (2.32.5)                                                                                                
Requirement already satisfied: pandas>=1.0.0 in /Users/mariospattichis/anaconda3/envs/homlp/lib/python3.12/site-packages (from torch-tb-profiler->-r /Users/mariospattichis/Library/CloudStorage/Dropbox/new-classes/python/handson-mlp/condaenv.zasdf3a6.requirements.txt (line 2)) (2.3.2)                                                                                  
Requirement already satisfied: tensorboard!=2.1.0,>=1.15 in /Users/mariospattichis/anaconda3/envs/homlp/lib/python3.12/site-packages (from torch-tb-profiler->-r /Users/mariospattichis/Library/CloudStorage/Dropbox/new-classes/python/handson-mlp/condaenv.zasdf3a6.requirements.txt (line 2)) (2.20.0)
Requirement already satisfied: idna in /Users/mariospattichis/anaconda3/envs/homlp/lib/python3.12/site-packages (from urlextract->-r /Users/mariospattichis/Library/CloudStorage/Dropbox/new-classes/python/handson-mlp/condaenv.zasdf3a6.requirements.txt (line 3)) (3.10)
Collecting uritools (from urlextract->-r /Users/mariospattichis/Library/CloudStorage/Dropbox/new-classes/python/handson-mlp/condaenv.zasdf3a6.requirements.txt (line 3))
  Downloading uritools-5.0.0-py3-none-any.whl.metadata (5.0 kB)
Requirement already satisfied: platformdirs in /Users/mariospattichis/anaconda3/envs/homlp/lib/python3.12/site-packages (from urlextract->-r /Users/mariospattichis/Library/CloudStorage/Dropbox/new-classes/python/handson-mlp/condaenv.zasdf3a6.requirements.txt (line 3)) (4.3.8)
Requirement already satisfied: filelock in /Users/mariospattichis/anaconda3/envs/homlp/lib/python3.12/site-packages (from urlextract->-r /Users/mariospattichis/Library/CloudStorage/Dropbox/new-classes/python/handson-mlp/condaenv.zasdf3a6.requirements.txt (line 3)) (3.19.1)
Requirement already satisfied: scipy in /Users/mariospattichis/anaconda3/envs/homlp/lib/python3.12/site-packages (from bitsandbytes->-r /Users/mariospattichis/Library/CloudStorage/Dropbox/new-classes/python/handson-mlp/condaenv.zasdf3a6.requirements.txt (line 4)) (1.16.1)
Requirement already satisfied: numpy>=1.21.6 in /Users/mariospattichis/anaconda3/envs/homlp/lib/python3.12/site-packages (from lap->-r /Users/mariospattichis/Library/CloudStorage/Dropbox/new-classes/python/handson-mlp/condaenv.zasdf3a6.requirements.txt (line 6)) (1.26.4)
Requirement already satisfied: python-dateutil>=2.8.2 in /Users/mariospattichis/anaconda3/envs/homlp/lib/python3.12/site-packages (from pandas>=1.0.0->torch-tb-profiler->-r /Users/mariospattichis/Library/CloudStorage/Dropbox/new-classes/python/handson-mlp/condaenv.zasdf3a6.requirements.txt (line 2)) (2.9.0.post0)
Requirement already satisfied: pytz>=2020.1 in /Users/mariospattichis/anaconda3/envs/homlp/lib/python3.12/site-packages (from pandas>=1.0.0->torch-tb-profiler->-r /Users/mariospattichis/Library/CloudStorage/Dropbox/new-classes/python/handson-mlp/condaenv.zasdf3a6.requirements.txt (line 2)) (2025.2)
Requirement already satisfied: tzdata>=2022.7 in /Users/mariospattichis/anaconda3/envs/homlp/lib/python3.12/site-packages (from pandas>=1.0.0->torch-tb-profiler->-r /Users/mariospattichis/Library/CloudStorage/Dropbox/new-classes/python/handson-mlp/condaenv.zasdf3a6.requirements.txt (line 2)) (2025.2)
Requirement already satisfied: six>=1.5 in /Users/mariospattichis/anaconda3/envs/homlp/lib/python3.12/site-packages (from python-dateutil>=2.8.2->pandas>=1.0.0->torch-tb-profiler->-r /Users/mariospattichis/Library/CloudStorage/Dropbox/new-classes/python/handson-mlp/condaenv.zasdf3a6.requirements.txt (line 2)) (1.17.0)
Requirement already satisfied: absl-py>=0.4 in /Users/mariospattichis/anaconda3/envs/homlp/lib/python3.12/site-packages (from tensorboard!=2.1.0,>=1.15->torch-tb-profiler->-r /Users/mariospattichis/Library/CloudStorage/Dropbox/new-classes/python/handson-mlp/condaenv.zasdf3a6.requirements.txt (line 2)) (2.3.1)
Requirement already satisfied: grpcio>=1.48.2 in /Users/mariospattichis/anaconda3/envs/homlp/lib/python3.12/site-packages (from tensorboard!=2.1.0,>=1.15->torch-tb-profiler->-r /Users/mariospattichis/Library/CloudStorage/Dropbox/new-classes/python/handson-mlp/condaenv.zasdf3a6.requirements.txt (line 2)) (1.73.1)
Requirement already satisfied: markdown>=2.6.8 in /Users/mariospattichis/anaconda3/envs/homlp/lib/python3.12/site-packages (from tensorboard!=2.1.0,>=1.15->torch-tb-profiler->-r /Users/mariospattichis/Library/CloudStorage/Dropbox/new-classes/python/handson-mlp/condaenv.zasdf3a6.requirements.txt (line 2)) (3.8.2)
Requirement already satisfied: packaging in /Users/mariospattichis/anaconda3/envs/homlp/lib/python3.12/site-packages (from tensorboard!=2.1.0,>=1.15->torch-tb-profiler->-r /Users/mariospattichis/Library/CloudStorage/Dropbox/new-classes/python/handson-mlp/condaenv.zasdf3a6.requirements.txt (line 2)) (25.0)
Requirement already satisfied: pillow in /Users/mariospattichis/anaconda3/envs/homlp/lib/python3.12/site-packages (from tensorboard!=2.1.0,>=1.15->torch-tb-profiler->-r /Users/mariospattichis/Library/CloudStorage/Dropbox/new-classes/python/handson-mlp/condaenv.zasdf3a6.requirements.txt (line 2)) (11.3.0)
Requirement already satisfied: protobuf in /Users/mariospattichis/anaconda3/envs/homlp/lib/python3.12/site-packages (from tensorboard!=2.1.0,>=1.15->torch-tb-profiler->-r /Users/mariospattichis/Library/CloudStorage/Dropbox/new-classes/python/handson-mlp/condaenv.zasdf3a6.requirements.txt (line 2)) (6.31.1)
Requirement already satisfied: setuptools>=41.0.0 in /Users/mariospattichis/anaconda3/envs/homlp/lib/python3.12/site-packages (from tensorboard!=2.1.0,>=1.15->torch-tb-profiler->-r /Users/mariospattichis/Library/CloudStorage/Dropbox/new-classes/python/handson-mlp/condaenv.zasdf3a6.requirements.txt (line 2)) (80.9.0)
Requirement already satisfied: tensorboard-data-server<0.8.0,>=0.7.0 in /Users/mariospattichis/anaconda3/envs/homlp/lib/python3.12/site-packages (from tensorboard!=2.1.0,>=1.15->torch-tb-profiler->-r /Users/mariospattichis/Library/CloudStorage/Dropbox/new-classes/python/handson-mlp/condaenv.zasdf3a6.requirements.txt (line 2)) (0.7.0)
Requirement already satisfied: werkzeug>=1.0.1 in /Users/mariospattichis/anaconda3/envs/homlp/lib/python3.12/site-packages (from tensorboard!=2.1.0,>=1.15->torch-tb-profiler->-r /Users/mariospattichis/Library/CloudStorage/Dropbox/new-classes/python/handson-mlp/condaenv.zasdf3a6.requirements.txt (line 2)) (3.1.3)
Requirement already satisfied: MarkupSafe>=2.1.1 in /Users/mariospattichis/anaconda3/envs/homlp/lib/python3.12/site-packages (from werkzeug>=1.0.1->tensorboard!=2.1.0,>=1.15->torch-tb-profiler->-r /Users/mariospattichis/Library/CloudStorage/Dropbox/new-classes/python/handson-mlp/condaenv.zasdf3a6.requirements.txt (line 2)) (3.0.2)
Requirement already satisfied: charset_normalizer<4,>=2 in /Users/mariospattichis/anaconda3/envs/homlp/lib/python3.12/site-packages (from requests->AutoROM->-r /Users/mariospattichis/Library/CloudStorage/Dropbox/new-classes/python/handson-mlp/condaenv.zasdf3a6.requirements.txt (line 1)) (3.4.3)
Requirement already satisfied: urllib3<3,>=1.21.1 in /Users/mariospattichis/anaconda3/envs/homlp/lib/python3.12/site-packages (from requests->AutoROM->-r /Users/mariospattichis/Library/CloudStorage/Dropbox/new-classes/python/handson-mlp/condaenv.zasdf3a6.requirements.txt (line 1)) (2.5.0)
Requirement already satisfied: certifi>=2017.4.17 in /Users/mariospattichis/anaconda3/envs/homlp/lib/python3.12/site-packages (from requests->AutoROM->-r /Users/mariospattichis/Library/CloudStorage/Dropbox/new-classes/python/handson-mlp/condaenv.zasdf3a6.requirements.txt (line 1)) (2025.8.3)
Downloading AutoROM-0.6.1-py3-none-any.whl (9.4 kB)
Downloading torch_tb_profiler-0.4.3-py3-none-any.whl (1.1 MB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 1.1/1.1 MB 12.2 MB/s  0:00:00
Downloading urlextract-1.9.0-py3-none-any.whl (21 kB)
Downloading bitsandbytes-0.42.0-py3-none-any.whl (105.0 MB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 105.0/105.0 MB 31.1 MB/s  0:00:03
Downloading lap-0.5.12-cp312-cp312-macosx_11_0_arm64.whl (1.5 MB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 1.5/1.5 MB 31.1 MB/s  0:00:00
Downloading uritools-5.0.0-py3-none-any.whl (10 kB)
Installing collected packages: uritools, lap, urlextract, bitsandbytes, AutoROM, torch-tb-profiler

Successfully installed AutoROM-0.6.1 bitsandbytes-0.42.0 lap-0.5.12 torch-tb-profiler-0.4.3 uritools-5.0.0 urlextract-1.9.0

done
#
# To activate this environment, use
#
#     $ conda activate homlp
#
# To deactivate an active environment, use
#
#     $ conda deactivate

(base) mariospattichis@Marioss-MacBook-Pro-802 handson-mlp %  conda activate homlp
(homlp) mariospattichis@Marioss-MacBook-Pro-802 handson-mlp % python3 -m ipykernel install --user --name=python3
Installed kernelspec python3 in /Users/mariospattichis/Library/Jupyter/kernels/python3
(homlp) mariospattichis@Marioss-MacBook-Pro-802 handson-mlp % jupyter lab
[I 2025-08-23 09:48:56.374 ServerApp] jupyter_lsp | extension was successfully linked.
[I 2025-08-23 09:48:56.376 ServerApp] jupyter_server_mathjax | extension was successfully linked.
[I 2025-08-23 09:48:56.378 ServerApp] jupyter_server_terminals | extension was successfully linked.
[I 2025-08-23 09:48:56.380 ServerApp] jupyterlab | extension was successfully linked.
[I 2025-08-23 09:48:56.380 ServerApp] nbdime | extension was successfully linked.
[I 2025-08-23 09:48:56.382 ServerApp] notebook | extension was successfully linked.
[I 2025-08-23 09:48:56.629 ServerApp] notebook_shim | extension was successfully linked.
[I 2025-08-23 09:48:56.660 ServerApp] notebook_shim | extension was successfully loaded.
[I 2025-08-23 09:48:56.662 ServerApp] jupyter_lsp | extension was successfully loaded.
[I 2025-08-23 09:48:56.662 ServerApp] jupyter_server_mathjax | extension was successfully loaded.
[I 2025-08-23 09:48:56.662 ServerApp] jupyter_server_terminals | extension was successfully loaded.
[I 2025-08-23 09:48:56.665 LabApp] JupyterLab extension loaded from /Users/mariospattichis/anaconda3/envs/homlp/lib/python3.12/site-packages/jupyterlab
[I 2025-08-23 09:48:56.665 LabApp] JupyterLab application directory is /Users/mariospattichis/anaconda3/envs/homlp/share/jupyter/lab
[I 2025-08-23 09:48:56.666 LabApp] Extension Manager is 'pypi'.
[I 2025-08-23 09:48:56.708 ServerApp] jupyterlab | extension was successfully loaded.
[I 2025-08-23 09:48:56.817 ServerApp] nbdime | extension was successfully loaded.
[I 2025-08-23 09:48:56.820 ServerApp] notebook | extension was successfully loaded.
[I 2025-08-23 09:48:56.837 ServerApp] Serving notebooks from local directory: /Users/mariospattichis/Library/CloudStorage/Dropbox/new-classes/python/handson-mlp
[I 2025-08-23 09:48:56.837 ServerApp] Jupyter Server 2.17.0 is running at:
[I 2025-08-23 09:48:56.837 ServerApp] http://localhost:8888/lab?token=5678126770e8f8cd35b5fbe22af8c71b340b131b4b08f9ee
[I 2025-08-23 09:48:56.837 ServerApp]     http://127.0.0.1:8888/lab?token=5678126770e8f8cd35b5fbe22af8c71b340b131b4b08f9ee
[I 2025-08-23 09:48:56.837 ServerApp] Use Control-C to stop this server and shut down all kernels (twice to skip confirmation).
[C 2025-08-23 09:48:56.883 ServerApp] 
    
    To access the server, open this file in a browser:
        file:///Users/mariospattichis/Library/Jupyter/runtime/jpserver-85647-open.html
    Or copy and paste one of these URLs:
        http://localhost:8888/lab?token=5678126770e8f8cd35b5fbe22af8c71b340b131b4b08f9ee
        http://127.0.0.1:8888/lab?token=5678126770e8f8cd35b5fbe22af8c71b340b131b4b08f9ee
[I 2025-08-23 09:48:59.336 ServerApp] Skipped non-installed server(s): bash-language-server, dockerfile-language-server-nodejs, javascript-typescript-langserver, jedi-language-server, julia-language-server, pyright, python-language-server, python-lsp-server, r-languageserver, sql-language-server, texlab, typescript-language-server, unified-language-server, vscode-css-languageserver-bin, vscode-html-languageserver-bin, vscode-json-languageserver-bin, yaml-language-server
[W 2025-08-23 09:48:59.548 LabApp] Could not determine jupyterlab build status without nodejs
[W 2025-08-23 09:48:59.728 ServerApp] 404 GET /api/contents/FFT-demos-2024.ipynb?content=0&hash=0&1755960539725 (bb609c6eead146b29d7cb838ea76cf54@127.0.0.1) 0.71ms referer=http://localhost:8888/lab
[W 2025-08-23 09:48:59.728 ServerApp] 404 GET /api/contents/FFT-demos-2024.ipynb?content=0&hash=0&1755960539725 (127.0.0.1): No such file or directory: FFT-demos-2024.ipynb
[W 2025-08-23 09:48:59.729 ServerApp] 404 GET /api/contents/FFT-demos-2024.ipynb?content=0&hash=0&1755960539725 (bb609c6eead146b29d7cb838ea76cf54@127.0.0.1) 0.50ms referer=http://localhost:8888/lab
[W 2025-08-23 09:48:59.729 ServerApp] 404 GET /api/contents/FFT-demos-2024.ipynb?content=0&hash=0&1755960539725 (127.0.0.1): No such file or directory: FFT-demos-2024.ipynb
[W 2025-08-23 09:49:05.748 ServerApp] Notebook 01_the_machine_learning_landscape.ipynb is not trusted
[I 2025-08-23 09:49:06.086 ServerApp] Kernel started: 5dab7ec9-c45a-4179-bebe-2a31200e9c66
[I 2025-08-23 09:49:07.059 ServerApp] Connecting to kernel 5dab7ec9-c45a-4179-bebe-2a31200e9c66.
[W 2025-08-23 09:49:07.060 ServerApp] The websocket_ping_timeout (90000) cannot be longer than the websocket_ping_interval (30000).
    Setting websocket_ping_timeout=30000
[I 2025-08-23 09:49:07.062 ServerApp] Connecting to kernel 5dab7ec9-c45a-4179-bebe-2a31200e9c66.
[I 2025-08-23 09:49:07.067 ServerApp] Connecting to kernel 5dab7ec9-c45a-4179-bebe-2a31200e9c66.
[I 2025-08-23 09:49:20.259 ServerApp] Kernel restarted: 5dab7ec9-c45a-4179-bebe-2a31200e9c66
[I 2025-08-23 09:49:20.263 ServerApp] Starting buffering for 5dab7ec9-c45a-4179-bebe-2a31200e9c66:e69f53ab-1b2a-4e5f-84a2-7829af377fc3
[I 2025-08-23 09:49:20.267 ServerApp] Connecting to kernel 5dab7ec9-c45a-4179-bebe-2a31200e9c66.
[I 2025-08-23 09:49:20.267 ServerApp] Restoring connection for 5dab7ec9-c45a-4179-bebe-2a31200e9c66:e69f53ab-1b2a-4e5f-84a2-7829af377fc3
```