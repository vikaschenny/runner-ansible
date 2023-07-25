    1  exit
    2  cat /etc/*release
    3  clear
    4  apt-get update
    5  docker
    6  clear
    7   apt-get install -y wget zip git unzip python3 
    8       apt-get update
    9       apt-get install ca-certificates curl gnupg curl -y
   10       echo      "deb [arch="$(dpkg --print-architecture)" signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
   11       "$(. /etc/os-release && echo "$VERSION_CODENAME")" stable" |      sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
   12       sudo apt-get update
   13       sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin -y
   14       sudo install -m 0755 -d /etc/apt/keyrings
   15       curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
   16       sudo chmod a+r /etc/apt/keyrings/docker.gpg
   17  clear
   18    apt-get install -y wget zip git unzip python3
   19    apt-get install ca-certificates curl gnupg curl -y
   20      echo      "deb [arch="$(dpkg --print-architecture)" signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
   21       "$(. /etc/os-release && echo "$VERSION_CODENAME")" stable" |      sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
   22  sudo apt-get update
   23  sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin -y
   24  service docker status
   25  update-alternatives --install /usr/bin/python python /usr/bin/python3 10
   26  python
   27       echo 'deb https://releases.ansible.com/ansible-runner/deb/ <trusty|xenial|stretch> main' > /etc/apt/sources.list.d/ansible.list
   28       apt-key adv --keyserver keyserver.ubuntu.com --recv 3DD29021
   29       apt-get update
   30       apt-get install ansible-runner -y
   31  ansible-runner
   32  apt install python3-ansible-runner
   33  pip install docker
   34  apt install python3-pip
   35  pip install docker
   36  pip install ansible-runner
   37  cd /opt/
   38  git clone https://github.com/vikaschenny/demo-runner.git
   39  ls
   40  cd demo-runner/
   41  ls
   42  more inventory.ini 
   43  ssh-keygen
   44  cd /root/.ssh/
   45  ls
   46  cat id_rsa.pub
   47  cat id_rsa.pub > authorized_keys
   48  cat authorized_keys
   49  cd
   50  cd /opt/demo-runner/
   51  ifconfig
   52  apt install net-tools
   53  ifconfig
   54  ping 193.168.33.31
   55  ping 193.168.33.30
   56  ping 193.168.33.31
   57  clear
   58  ls
   59  more inventory.ini 
   60  ansible-playbook playbook.yml -i "192.168.33.11," --user vagrant --password vagrant
   61  ansible-playbook playbook.yml -i "192.168.33.11" --user vagrant --password vagrant
   62  ls
   63  vi demoinventory.ini 
   64  more demoinventory.ini 
   65  more playbook.yml 
   66  ansible-runner run -p playbook.yml -i demoinventory.ini --hosts=192.168.33.11 --env "ansible_user=vagrant ansible_password=vagrant"
   67  ansible-runner run -p playbook.yml -i demoinventory.ini --h 192.168.33.11 --env "ansible_user=vagrant ansible_password=vagrant"
   68  ansible-runner run -p playbook.yml -i demoinventory.ini --hosts "192.168.33.11" --env "ansible_user=vagrant ansible_password=vagrant"
   69  ansible-runner run -p playbook.yml -i demoinventory.ini --hosts=192.168.33.11 --env-vars "ansible_user=vagrant ansible_password=vagrant"
   70  ansible-runner run -p playbook.yml -i demoinventory.ini --hosts 192.168.33.11 --env-vars "ansible_user=vagrant ansible_password=vagrant"
   71  clear
   72  ansible-runner run -p playbook.yml -i demoinventory.ini --hosts=192.168.33.11 --extravars "ansible_user=vagrant ansible_password=vagrant"
   73  ansible-runner run -p playbook.yml -i demoinventory.ini --hosts=192.168.33.11 -e "ansible_user=vagrant ansible_password=vagrant"
   74  clear
   75  ls
   76  ansible-runner run -p playbook.yml -i demoinventory.ini --hosts=192.168.33.11  --extra-vars "ansible_user=vagrant ansible_password=vagrant"
   77  ansible-runner --version 
   78  pip install ansible-runner
   79  pip install ansible-runner:2.3.3
   80  clear
   81  ansible-runner run -p playbook.yml -i demoinventory.ini --hosts=192.168.33.11  --extra-vars "ansible_user=vagrant ansible_password=vagrant"
   82  ansible-runner --help
   83  ansible-runner run -p playbook.yml -i demoinventory.ini --hosts=192.168.33.11  --extra-vars "ansible_user=vagrant ansible_password=vagrant"
   84  ls
   85  vi entrypoint.sh 
   86  vi dockerfile 
   87  vi entrypoint.sh 
   88  vi dockerfile 
   89  mv dockerfile dockerfile.bkp
   90  vi dockerfile
   91  vi entrypoint.sh 
   92  ls
   93  docker images
   94  clear
   95  ls
   96  docker build -t demo-runner:1.0 .
   97  more playbook.yml 
   98  docker demo-runner:1.0 192.168.1.100 vagrant vagrant
   99  docker run demo-runner:1.0 192.168.1.100 vagrant vagrant
  100  vi entrypoint.sh 
  101  vi dockerfile
  102  docker build -t demo-runner:1.0 .
  103  docker run demo-runner:1.0 192.168.1.100 vagrant vagrant
  104  docker run -itd demo-runner:1.0 
  105  docker exec -it eaacbc461e7396635ae671568993c8afe09081c43472e0fc8cb4aa5ed6580377 bash
  106  docker ps
  107  docker ps -a
  108  docker rm $(docker ps -a -q)
  109  docker images
  110  docker rmi 87137c1fe4c6
  111  docker images
  112  ls
  113  vi dockerfile
  114  ./entrypoint.sh 192.168.1.100 vagrant vagrant
  115  ls
  116  more inventory.ini 
  117  vi entrypoint.sh 
  118  ./entrypoint.sh 192.168.1.100 vagrant vagrant
  119  vi entrypoint.sh 
  120  ./entrypoint.sh 192.168.1.100 vagrant vagrant
  121  ls
  122  more inventory.ini 
  123  ./entrypoint.sh 192.168.1.10 vagrant vagrant
  124  rm -rf demo-runner/
  125  ./entrypoint.sh 192.168.1.10 vagrant vagrant
  126  rm -rf demo-runner/
  127  rm -f inventory.ini 
  128  ./entrypoint.sh 192.168.1.10 vagrant vagrant
  129  vi entrypoint.sh 
  130  rm -rf demo-runner/
  131  rm -f inventory.ini 
  132  ./entrypoint.sh 192.168.1.10 vagrant vagrant
  133  ls
  134  vi entrypoint.sh 
  135  cd ..
  136  ls
  137  cd -
  138  ls
  139  ./entrypoint.sh 192.168.1.10 vagrant vagrant
  140  rm -rf demo-runner/
  141  rm -f inventory.ini 
  142  ./entrypoint.sh 192.168.1.10 vagrant vagrant
  143  cd ..
  144  ls
  145  more inventory.ini 
  146  vi entrypoint.sh 
  147  cd -
  148  vi entrypoint.sh 
  149  chmod 777 entrypoint.sh 
  150  ls
  151  rm -f ../inventory.ini 
  152  rm rf demo-runner/
  153  rm -rf demo-runner/
  154  ls
  155  ./entrypoint.sh 
  156  more entrypoint.sh 
  157  vi entrypoint.sh 
  158  ./entrypoint.sh 
  159  rm -rf demo-runner/
  160  rm -f ../inventory.ini 
  161  ./entrypoint.sh 
  162  ansible-runner run /opt/demo-runner/ -i /opt/inventory.ini 
  163  ansible-runner run -p /opt/demo-runner/ -i /opt/inventory.ini 
  164  ansible-runner run  /opt/demo-runner/ -p /opt/demo-runner/playbook.yml -i /opt/inventory.ini 
  165  ls ../
  166  chmod 777 ../inventory.ini 
  167  ansible-runner run  /opt/demo-runner/ -p /opt/demo-runner/playbook.yml -i /opt/inventory.ini 
  168  more ../inventory.ini 
  169  ls
  170  ./entrypoint.sh 
  171  rm -rf demo-runner/
  172  rm -f ../inventory.ini 
  173  ./entrypoint.sh 192.168.1.10 vagrant vagrant
  174  ansible-runner run  /opt/demo-runner/ -p /opt/demo-runner/playbook.yml -i /opt/inventory.ini 
  175  more ../inventory.ini 
  176  ansible-runner run  /opt/demo-runner/ -p /opt/demo-runner/playbook.yml -i /opt/inventory.ini 
  177  vi entrypoint.sh 
  178  ls
  179  rm -rf demo-runner/
  180  rm -f ../inventory.ini 
  181  ./entrypoint.sh 192.168.1.10 vagrant vagrant
  182  ls
  183  rm -rf demo-runner/
  184  ls
  185  rm -rf ../inventory.ini 
  186  ls
  187  docker images
  188  docker rmi 40bc7a6f9c8b
  189  ls
  190  docker images
  191  docker build -t demo-runner:1.0 .
  192  docker run demo-runner:1.0 192.168.1.100 vagrant vagrant
  193  ls 
  194  ./entrypoint.sh 
  195  more ../inventory.ini 
  196  rm -f ../inventory.ini 
  197  ip -o -4 addr show $(hostname -I | awk '{print $1}') | awk '{print $4}'
  198  ls
  199  docker run demo-runner:1.0 192.168.1.100 vagrant vagrant
  200  rm -f ../inventory.ini 
  201  ./entrypoint.sh 192.168.1.100 vagrant vagrant
  202  rm -rf demo-runner/
  203  rm -f ../inventory.ini 
  204  192.168.1.100 vagrant vagrant
  205  ./entrypoint.sh 192.168.1.100 vagrant vagrant
  206  more ../inventory.ini 
  207  vi entrypoint.sh 
  208  docker build -t demo-runner:1.0 .
  209  docker run demo-runner:1.0 192.168.1.11 vagrant vagrant
  210  docker ps
  211  docker ps -a
  212  docker start 9e2c62c78094
  213  docker ps -a
  214  vi entrypoint.sh 
  215  vi dockerfile
  216  docker build -t demo-runner:1.0 .
  217  docker run -itd demo-runner:1.0 
  218  docker ps
  219  docker exec -it c570f5a0ed40 bash
  220  ls
  221  more ../inventory.ini 
  222  docker images
  223  docker exec -it c570f5a0ed40 bash
  224  ls
  225  git status
  226  vi inventory.ini
  227  git status
  228  rm -rf 1
  229  rm -rf demo-runner/
  230  git status
  231  more inventory.ini 
  232  ls
  233  git add .
  234  git commit -m "update work "
  235  git push
  236  git pull
  237  mkdir demo
  238  cd ..
  239  ls
  240  mkdir demo
  241  cd demo
  242  git clone https://github.com/vikaschenny/demo-runner.git
  243  cd demo-runner/
  244  ls
  245  cp ../../demo-runner/entrypoint.sh .
  246  more entrypoint.sh 
  247  ls
  248  mv dockerfile dockerfile.bkp
  249  cp ../../demo-runner/dockerfile .
  250  l
  251  moe dockerfile
  252  more dockerfile
  253  ls
  254  clear
  255  git status
  256  git add .
  257  git commit -m " update docker file and entry sh file "
  258  git push
  259  ls
  260  ./entrypoint.sh 
  261  more entrypoint.sh 
  262  ;s
  263  ls
  264  cd ..
  265  ls
  266  cd demo-runner/
  267  cd ../
  268  cd ..
  269  ls
  270  cd demo-runner/
  271  ls
  272  more inventory.ini 
  273  more entrypoint.sh 
  274  ./entrypoint.sh 
  275  cd ..
  276  ls
  277  more inventory.ini 
  278  cd -
  279  more entrypoint.sh 
  280  rm -f ../inventory.ini 
  281  ./entrypoint.sh 192.168.33.11 vagrant vagrant 
  282  moe ../inventory.ini 
  283  more ../inventory.ini 
  284  ls
  285  vi entrypoint.sh 
  286  rm -f ../inventory.ini 
  287  rm -rf demo-runner/
  288  ./entrypoint.sh 192.168.33.11 vagrant vagrant 
  289  rm -f ../inventory.ini 
  290  rm -f inventory.ini 
  291  vi entrypoint.sh 
  292  ./entrypoint.sh 192.168.33.11 vagrant vagrant 
  293  ls
  294  more inv.ini 
  295  more entrypoint.sh 
  296  ansible-runner run /tmp/demo-runner -p /opt/demo-runner/playbook.yml -i inv.ini 
  297  ansible-runner run /tmp/demo-runner -p /opt/demo-runner/playbook.yml -i /path/to/inv.ini
  298  ansible-runner run /tmp/demo-runner -p /opt/demo-runner/playbook.yml -i inv.ini
  299  vi playbook.yml 
  300  ls
  301  more demo_create_container.py 
  302  ls
  303  more dockerfile
  304  ls
  305  more entrypoint.sh 
  306  ansible-runner run /tmp/demo-runner -p /opt/demo-runner/playbook.yml -i inv.ini
  307  chmod +r inv.ini 
  308  ansible-runner run /tmp/demo-runner -p /opt/demo-runner/playbook.yml -i inv.ini
  309  vi inv.ini 
  310  ansible-runner run /tmp/demo-runner -p /opt/demo-runner/playbook.yml -i inv.ini
  311  vi playbook.yml 
  312  vi inv.ini 
  313  ls
  314  apt-get install ansible
  315  find / -name ansible.cfg
  316  sudo apt-add-repository ppa:ansible/ansible
  317  sudo apt update
  318  sudo apt install ansible
  319   apt -f install
  320  ansible-runner run /tmp/demo-runner -p /opt/demo-runner/playbook.yml -i inv.ini
  321  vi /etc/ansible/ansible.cfg 
  322  ansible-runner run /tmp/demo-runner -p /opt/demo-runner/playbook.yml -i inv.ini
  323   ansible-runner --version
  324   ansible-runner -v
  325  ansible-runner --debug
  326  sudo apt remove ansible
  327  apt remove ansible-runner
  328  pip install ansible-runner
  329  pip uninstall ansible-runner
  330  dnf
  331  apt install dnf
  332  sudo apt install ansible
  333  dnf install python-ansible-runner
  334  cat /etc/*release
  335  echo 'deb https://releases.ansible.com/ansible-runner/deb/ <trusty|xenial|stretch> main' > /etc/apt/sources.list.d/ansible.list
  336  apt-key adv --keyserver keyserver.ubuntu.com --recv 3DD29021
  337  apt-get update
  338  apt-get install ansible-runner
  339  add-apt-repository ppa:mc3man/xerus-media
  340   apt -f install
  341  add-apt-repository ppa:mc3man/xerus-media
  342  sudo apt-get update
  343  apt remove ansible
  344  clear
  345  ls
  346  more dockerfile
  347  clear
  348  ls
  349  pip install ansible
  350  pip install ansible-core
  351  pip install ansible-runner
  352  ansible-runner
  353  pip show ansible-runner
  354  find / -name ansible-runner
  355  ln -s /usr/local/bin/ansible-runner /usr/bin/ansible-runner
  356  ansible-runner 
  357  ansible-runner clear
  358  cls
  359  clear
  360  ls
  361  ansible-runner run /tmp/demo-runner -p /opt/demo-runner/playbook.yml -i inv.ini
  362  more inv.ini 
  363  vi inv.ini 
  364  vi playbook.yml 
  365  ansible-runner run /tmp/demo-runner -p /opt/demo-runner/playbook.yml -i inv.ini
  366  ls
  367  clear
  368  ls
  369  more create_container.py 
  370  docker ps
  371  docker exec -it c570f5a0ed40 bash
  372  ls
  373   ansible-runner run /tmp/demo-runner -p /opt/demo-runner/playbook.yml -i inventory.ini
  374   ansible-runner run /tmp/demo-runner -p /opt/demo-runner/playbook.yml -i inv.ini 
  375  more inv.ini 
  376  more playbook.yml 
  377   ansible-runner -p /opt/demo-runner/playbook.yml -i inventory.ini run /tmp/demo-runner
  378   ansible-runner -p playbook.yml -i inv.ini run /tmp/demo-runner
  379  ansible-runner -p playbook.yml -i inv.ini run .
  380  ansible-runner run . -p playbook.yml -i inv.ini 
  381  cler
  382  clear
  383  ls
  384  more create_container.py 
  385  ls
  386  docker pull vikaschenny/ansible-builder:demo
  387  ansible-navigator run playbook.yml  --eei vikaschenny/ansible-builder:demo --pp never -b -m stdout
  388  ansible-runner run playbook.yml  --eei vikaschenny/ansible-builder:demo --pp never -b -m stdout
  389  pip install ansible-navigator
  390  ansible-navigator run playbook.yml  --eei vikaschenny/ansible-builder:demo --pp never -b -m stdout
  391  vi playbook.yml 
  392  ansible-navigator run playbook.yml  --eei vikaschenny/ansible-builder:demo --pp never -b -m stdout
  393  cat /var/log/syslog 
  394  vi playbook.yml 
  395  ansible-navigator run playbook.yml  --eei vikaschenny/ansible-builder:demo --pp never -b -m stdout
  396  clear
  397  ls
  398  more create_container.py 
  399  ls
  400  more dockerfile
  401  ls
  402  more entrypoint.sh 
  403  ansible-runner run /opt/demo-runner/ -p playbook.yml -i inv.ini 
  404  ls
  405  docker images
  406  more dockerfile
  407  ls
  408   more entrypoint.sh 
  409  vi dockerfile
  410  ls
  411  more entrypoint.sh 
  412  docker build -t demo-runner:1.0 .
  413  docker demo-runner:1.0 192.168.1.100 vagrant vagrant
  414  docker run demo-runner:1.0 192.168.1.100 vagrant vagrant
  415  ansible-runner run /opt/demo-runner/ -p playbook.yml -i inv.ini 
  416  docker images
  417  vikaschenny/ansible-builder   demo      9e6026ed2657   7 weeks ago     1.18GB
  418  ansible-navigator run playbook.yml  --eei vikaschenny/ansible-builder:demo --pp never -b -m stdout
  419  ls
  420  more dockerfile
  421  more entrypoint.sh 
  422  clear
  423  ls
  424  pwd
  425  ls
  426  more inv.ini 
  427  grep '\[legacy\]' inv.ini -A 1 | grep -v '\[legacy\]'
  428  docker images
  429  ls
  430  ansible-runner -p playbook.yml --hosts localhost --runner-image vikaschenny/ansible-builder:demo
  431  ansible-runner run -p playbook.yml --hosts localhost --runner-image vikaschenny/ansible-builder:demo
  432  cd ..
  433  ls
  434  mkdir one
  435  cd one/
  436  ls
  437  vi playbook.yaml
  438  vi hosts.ini
  439  vi run_playbook.sh
  440  ls
  441  rm -f 1
  442  ls
  443  chmod 777 *
  444  ls
  445  chmod +x run_playbook.sh
  446  ./run_playbook.sh 
  447  ld
  448  ls
  449  mv playbook.yaml playbook.yml 
  450  ls
  451  ./run_playbook.sh 
  452  ls
  453  more run_playbook.sh 
  454  docker ps -a
  455  docker rm $(docker ps -a -q)
  456  docker ps
  457  clear
  458  ls
  459  cd /root/.ssh/
  460  ls
  461  more authorized_keys 
  462  cat id_rsa.pub >> authorized_keys 
  463  more authorized_keys 
  464  cd
  465  cd /opt/one/
  466  ls
  467  ssh localhost
  468  ifconfig
  469  ssh 10.0.2.15
  470  cat /root/.ssh/id_rsa.pub 
  471  exit
  472  ssh vagrant@10.0.2.15
  473  cd /opt/one/
  474  ls
  475  vi hosts.ini 
  476  ifconfig
  477  vi hosts.ini 
  478  ls
  479  ./run_playbook.sh 
  480  ssh vagrant@10.0.2.15
  481  ./run_playbook.sh 
  482  exit
  483  cd /opt/one/
  484  ./run_playbook.sh 
  485  exit
  486  ls
  487  cd /opt/
  488  ls
  489  cd /
  490  ls
  491  cd
  492  ls
  493  cd /opt/
  494  ls
  495  exit
  496  cd /opt/one
  497  ls
  498  ./run_playbook.sh 
  499  more run_playbook.sh 
  500  more hosts.ini 
  501  ping 192.168.33.11
  502  ping 192.168.33.31
  503  vi hosts.ini 
  504  ./run_playbook.sh 
  505  more run_playbook.sh 
  506  vi run_playbook.sh 
  507  SERVER_IPS=($(awk '/\[server\]/{f=1; next} /\[/{f=0} f {print $1}' hosts.ini))
  508  vi run_playbook.sh 
  509  ./run_playbook.sh 
  510  ls
  511  more nhosts.ini 
  512  more hosts.ini 
  513  grep -oP "(?<=ansible_username=).*" hosts.ini
  514  grep ansible_username hosts.ini
  515  vi run_playbook.sh 
  516  ./run_playbook.sh 
  517  more nhosts.ini 
  518  vi run_playbook.sh 
  519  ./run_playbook.sh 
  520  more run_playbook.sh 
  521  vi run_playbook.sh 
  522  exit
  523  cd /opt/
  524  ls
  525  cd one/
  526  ls
  527  docker ps -w
  528  docker ps -a -w
  529  docker ps -a -watch
  530  vi run_playbook.sh 
  531  docker ps
  532  docker ps -a
  533  ./run_playbook.sh 
  534  docker ps
  535  docker ps -a
  536  docker logs -f ed230a954b46
  537  docker logs -f 8b01206d1f02
  538  vi hosts.ini 
  539  more run_playbook.sh 
  540  $(awk '/\[server\]/{f=1; next} /\[/{f=0} f {print $1}' hosts.ini
  541  awk '/\[server\]/{f=1; next} /\[/{f=0} f {print $1}' hosts.ini
  542  vi run_playbook.sh 
  543  ./run_playbook.sh 
  544  docker logs -f 39512c2df487716bd7f93ddf3f0b81389f69871f397aade55d957568786fb50c
  545  docker logs -f dd5ccbd2e802addeff04e108fbb1f40c708570754fc21010d56054c24d82b5bc
  546  vi run_playbook.sh 
  547  ./run_playbook.sh 
  548  docker logs -f ef1710d82054351a143f9d5b41edfe8339b730b726930a7795fbda130f6edcff
  549  docker logs -f f6fc9372ce1267f2f880b2b1407848b8d761f5deaadf52a3691e588817dc1c2b
  550  ls
  551  vi run_playbook.sh 
  552  ./run_playbook.sh 
  553  ls
  554  vi run_playbook.sh 
  555  ./run_playbook.sh 
  556  ls
  557  rm -rf 10.0.2.15_*
  558  rm -rf 192.168.33.11_*
  559  ls
  560  rm -f nhosts.ini 
  561  ls
  562  clear
  563  ls
  564  docker ps -a
  565  docker rm $(docker ps -a )
  566  docker rm $(docker ps -a -q)
  567  cls
  568  clear
  569  ls
  570  ./run_playbook.sh 
  571  docker ps
  572  docker ps -a
  573  docker logs -f ff0691a55fdd
  574  docker logs -f a811a52f4b00
  575  ls
  576  more run_playbook.sh 
  577  vi run_playbook.sh 
  578  ./run_playbook.sh 
  579  docker logs -f 9e7a66da1b06d7cb551fb63d1e4508c9c1f0eeee4b6ad62de0770516e836dc47
  580  ./run_playbook.sh 
  581  docker rm $(docker ps -a -q)
  582  vi run_playbook.sh 
  583  ./run_playbook.sh 
  584  ls
  585  ./run_playbook.sh 
  586  ls
  587  vi run_playbook.sh 
  588  ./run_playbook.sh 
  589  docker logs -f 377bf53ccb96645f4d8b3053ce2fcd09cf23c0df87c2c1dd9618c0c9aefd562f
  590  vi run_playbook.sh 
  591  l
  592  vi run_playbook.sh 
  593  ./run_playbook.sh 
  594  docker logs -f a133b5bfd05fee38f67f071edc2ad4a8c4c9047bbc95f42588f754992a3833fa
  595  ansible-navigator run playbook.yml  --eei vikaschenny/ansible-builder:demo --pp never -b -m stdout
  596  docker ps
  597  docker ps -a
  598  docker rm $(docker ps -a -q)
  599  docker ps -a
  600  ansible-navigator run playbook.yml  --eei vikaschenny/ansible-builder:demo --pp never -b -m stdout
  601  docker ps -a
  602  docker ps
  603  vi run_playbook.sh 
  604  apt-get removeansible 
  605  apt-get remove ansible 
  606  apt-get remove ansible-runner
  607  pip unstall ansbile-runner
  608  pip uninstall ansbile-runner
  609  ansible-runner
  610  rm -f /usr/bin/ansible-runner 
  611  ansible-runner
  612  pip uninstall ansible-runner
  613  ansible-runner
  614  clear
  615  ls
  616  rm -f ansible-navigator.log 
  617  rm -f playbook-artifact-2023-07-04T11\:21\:*
  618  ls
  619  clear
  620  ls
  621  rm -f 10.0.2.15_hosts.ini 192.168.33.11_hosts.ini
  622  clea
  623  clear
  624  ls
  625  ./run_playbook.sh 
  626  docker logs -f a747e93cd91b0923564eaaa63e9caf99d82bb1e194be9e95e79bebf578d932b8
  627  docker logs -f 4e2e99b87cbe52992601b24e3d98d8d6d7348b95bfad7cb24c3ee56e0e689f63
  628  ls
  629  pip install ansible-runner
  630  ansible-runner 
  631  clear
  632  ansible-runner run -p playbook.yml
  633  ansible-runner run /opt/demo-runner/ -p playbook.yml 
  634  ls
  635  vi run_playbook.sh 
  636  ls
  637  vi playbook.yml 
  638  vi run_playbook.sh 
  639  ./run_playbook.sh 
  640  docker logs -f a2b0f10b545381d178b5677b1385f57c8193cb887c797b117915b9bd0e07f748
  641  vi run_playbook.sh 
  642  ./run_playbook.sh 
  643  docker logs -f cd4ce7a5ebd2a2dcb31ea93c3e22af29bdb983728d4231632bb271f0ec0c922d
  644  docker logs -f 6f2feeddd7c9d85f395041f44e25eb660f9235b65f921f9225d093465fd2dbc4
  645  cd ..
  646  ls
  647  getsystedetails.sh
  648  vi getsystedetails.sh
  649  chmod 777 getsystedetails.sh 
  650  ./getsystedetails.sh 
  651  vi getsystedetails.sh
  652  ./getsystedetails.sh 
  653  clear
  654  ls
  655  more getsystedetails.sh 
  656  ./getsystedetails.sh 
  657  ls
  658  vi getsystedetails.sh 
  659  c one/
  660  cd one/
  661  ls
  662  more run_playbook.sh 
  663  vi run_playbook.sh 
  664  docker ps
  665  docker ps -a
  666  docker rm $(docker ps -a -q)
  667  ls
  668  ./run_playbook.sh 
  669  docker logs -f e59c5d15ba70dfac4389fccca49c8dde5c80d8f90037e4d73fd2b48ec5a876c1
  670  docker logs -f 316dfc516216a8fb4c7faae269de4bcdf49395b761f209a808fc6ccca64163d6
  671  more hosts.ini 
  672  vi run_playbook.sh 
  673  docker ps -a
  674  apt-get install dnf
  675  docker images
  676  docker run -v $(pwd):/runner -v /path/to/inventory_file:/etc/ansible/hosts -d vikaschenny/ansible-builder:demo ansible-runner playbook.yml
  677  docker logs -f 8ce8b1c0f72cfec2cf621cf9ec9cd02f08252cd888e4c7dea79851d4822f502f
  678  docker run -v $(pwd):/runner -v /path/to/inventory_file:/etc/ansible/hosts -d vikaschenny/ansible-builder:demo ansible-runner playbook.yml
  679  docker run -v $(pwd):/runner -v /path/to/inventory_file:/etc/ansible/hosts -it vikaschenny/ansible-builder:demo ansible-runner playbook.yml
  680  clear
  681  cd ..
  682  ls
  683  git clone https://github.com/vikaschenny/ansible-runner.git
  684  cd ansible-runner/
  685  ls
  686  git status
  687  git branch
  688  git checkout demo
  689  ls
  690  cd demo/
  691  ls
  692  clear
  693  ls
  694  cd context
  695  ls
  696  more Dockerfile 
  697  cd ..
  698  ls
  699  mv context context.bkp1
  700  ls
  701  more ansible-navigator.log 
  702  clear
  703  ls
  704  rm -f ansible-navigator.log
  705  ls
  706  more requirements.txt 
  707  more requirements.yml 
  708  clear
  709  ls
  710  more playbook.yaml 
  711  clear
  712  ls
  713  more execution-environment.yml 
  714  more bindep.txt 
  715  ls
  716  vi bindep.txt 
  717  vi requirements.txt 
  718  vi requirements.yml 
  719  more requirements.yml 
  720  ls
  721  more execution-environment.yml 
  722  ansible-builder build --tag vikaschenny/ee-trianz:v1.0
  723  ls
  724  vi requirements.txt 
  725  ansible-builder build --tag vikaschenny/ee-trianz:v1.0
  726  docker images
  727  ls
  728  cd context
  729  ls
  730  more Dockerfile 
  731  ls
  732  docker run -v $(pwd):/runner -v /path/to/inventory_file:/etc/ansible/hosts -d vikaschenny/ee-trianz:v1.0 ansible-runner playbook.yml
  733  docker ps -a
  734  docker rm $(docker ps -a -q)
  735  docker ps
  736  docker ps -a
  737  history
  738  cd ../../
  739  ls
  740  cd ..
  741  ls
  742  cd one/
  743  ls
  744  vi run_playbook.sh 
  745  ./run_playbook.sh 
  746  docker logs -f b138d77e54e31dd44e46809732c7e0584a819e0d264582d037b527eaaa1bc7f9
  747  vi run_playbook.sh 
  748  clear
  749  ls
  750  docker ps -a
  751  docker rm $(docker ps -a -q)
  752  ./run_playbook.sh 
  753  docker logs -f fdebe47bebfee33b7cb6177bc13ee612c4376a987aba151c322f69ca40949fcd
  754  docker logs -f e38ff1b4bd062a3d6c28ebce993026d73bbaee8124de11664d66d99a74710aa7
  755  ssh vagrant@192.168.33.11
  756  ssh vagrant@10.0.2.15
  757  ssh vagrant@192.168.33.11
  758  ssh-keygen -f "/root/.ssh/known_hosts" -R "192.168.33.11"
  759  ssh vagrant@192.168.33.11
  760  ls /root/.ssh/
  761  cat  /root/.ssh/authorized_keys 
  762  ssh vagrant@192.168.33.11
  763  exit
  764  cd /opt/one/
  765  ls
  766  ssh vagrant@192.168.33.11
  767  restorecon -r -vv .ssh/authorized_keys
  768  restorecon -r -vv /root/.ssh/authorized_keys
  769  apt install policycoreutils
  770  restorecon -r -vv /root/.ssh/authorized_keys
  771  ssh vagrant@192.168.33.11
  772  exit
  773  ls
  774  cd /op
  775  cd /opt/one/
  776  ls
  777  cd ..
  778  ls
  779  cd demo-runner/
  780  ls
  781  cd ..
  782  ls
  783  cd ansible-runner/
  784  ls
  785  clear
  786  ls
  787  cd ..
  788  ls
  789  cd demo
  790  ls
  791  cd demo-runner/
  792  ls
  793  cd
  794  cd /op
  795  cd /opt/
  796  ls
  797  cd one/
  798  ls
  799  cd ..
  800  ls
  801  clear
  802  ls
  803  cd one/
  804  ls
  805  docker images
  806  dive vikaschenny/ee-trianz:v1.0
  807  ls
  808  vi run_playbook.sh 
  809  docker ps -a
  810  docker rm $(docker ps -a -q)
  811  clera
  812  clear
  813  docker ps -a
  814  docker ps 
  815  ls
  816  ./run_playbook.sh 
  817  docker ps -a
  818  docker logs -f 4707de96b349
  819  docker logs -f 8bc5e9cfcc50
  820  ls
  821  more run_playbook.sh 
  822  vi run_playbook.sh 
  823  ls
  824  more playbook.yml 
  825  vi run_playbook.sh 
  826  ls
  827  cd ..
  828  ls
  829  cd ansible-runner/
  830  ls
  831  cd demo/
  832  ls
  833  vi execution-environment.yml 
  834  more /opt/one/run_playbook.sh 
  835  vi execution-environment.yml 
  836  ls
  837  mv context context.07072023
  838  ls
  839  ansible-builder build --tag vikaschenny/ee-trianz:v1.0
  840  clear
  841  ls
  842  cd
  843  ls
  844  git clone https://github.com/ansible/ansible-runner.git
  845  cd ansible-runner
  846  wget https://github.com/ansible/ansible-runner/archive/refs/tags/2.3.3.tar.gz
  847  ls
  848  cd ..
  849  ls
  850  wget https://github.com/ansible/ansible-runner/archive/refs/tags/2.3.3.tar.gz
  851  ls
  852  tar -xvzf 2.3.3.tar.gz 
  853  ls
  854  cd ansible-runner-2.3.3/
  855  ls
  856  more Dockerfile 
  857  clear
  858  ls
  859  more bindep.txt 
  860  clear
  861  ls
  862  cd ansible_runner/
  863  ls
  864  cd ..
  865  ls
  866  sudo apt-get install python3 python3-pip python3-dev gcc
  867  python3 -m venv venv
  868  source venv/bin/activate
  869  apt install python3.10-venv
  870  python3 -m venv venv
  871  source venv/bin/activate
  872  ansible-runner --version
  873  pip install .
  874  ls
  875  more Makefile 
  876  pip install wheel
  877  ls
  878  cd ..
  879  ls
  880  rm -rf ansible-runner-2.3.3/
  881  exit
  882  ls
  883  tar -xvzf 2.3.3.tar.gz 
  884  ls
  885  cd ansible-runner-2.3.3/
  886  ls
  887  vi Makefile 
  888  ls
  889  source venv/bin/activate
  890  python3 -m venv venv
  891  source venv/bin/activate
  892  pip install -r requirements.txt
  893  python3 setup.py install
  894  pip install wheel
  895  python3 setup.py install
  896  pip install --use-pep517
  897  exit
  898  ls
  899  cd ansible-runner-2.3.3/
  900  python3 setup.py bdist_wheel
  901  ls
  902  vi setup.cfg 
  903  ls
  904  more Makefile 
  905  ls
  906  make
  907  clear
  908  ls
  909  python3 setup.py bdist_wheel
  910  pip uninstall ansible-runner
  911  python3 setup.py bdist_wheel
  912  pip uninstall ansible-runner
  913  ansible-runner
  914  clear
  915  python3 -m venv venv
  916  source venv/bin/activate
  917  pip install -r requirements.txt
  918  python3 setup.py install
  919  pip install --use-pep517
  920  export PBR_VERSION=1.2.3
  921  python3 setup.py install
  922  pip install .
  923  ansible-runner --version
  924  pip uninstall .
  925  ansible-version
  926  exit
  927  ls
  928  history
  929  ls
  930  cd /op
  931  ls
  932  cd /opt/
  933  ls
  934  cd
  935  clear
  936  ls
  937  cd birru-build/
  938  ls
  939  cd ansible-runner/
  940  ls
  941  clear
  942  ls
  943  vi Dockerfile 
  944  ls
  945  clear
  946  ls
  947  vi Makefile 
  948  l
  949  docker images
  950  docker ps
  951  docker ps -a
  952  docker rm $(docker ps -a -q)
  953  ls
  954  git remove -v
  955  git remote -v
  956  git tag
  957  ls
  958  vi Makefile 
  959  make image
  960  ls
  961  vi Dockerfile 
  962  docker images
  963  cd /opt/
  964  ls
  965  cd demo
  966  ls
  967  cd demo-runner/
  968  ls
  969  cd ..
  970  ls
  971  cd ..
  972  ls
  973  cd /opt/ansible-runner/demo
  974  ls
  975  vi execution-environment.yml 
  976  more requirements.txt 
  977  more requirements.yml 
  978  docker images
  979  ansible-builder -t vikaschenny/trianz-ee-demo:v1.0
  980  ansible-builder -t vikaschenny/trianz-ee-demo:v1.0 .
  981  history
  982  ansible-builder build --tag vikaschenny/ee-trianz:v1.0
  983  vi execution-environment.yml 
  984  cd /opt/one/
  985  ls
  986  vi run_playbook.sh 
  987  $ sudo apt install -y curl gnupg2 software-properties-common apt-transport-https ca-certificates
  988  sudo apt install -y curl gnupg2 software-properties-common apt-transport-https ca-certificates
  989  curl -s https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo gpg --dearmour -o /etc/apt/trusted.gpg.d/kubernetes-xenial.gpg
  990  apt-add-repository "deb http://apt.kubernetes.io/ kubernetes-xenial main"
  991  apt update
  992  vi /etc/apt/sources.list
  993  cd /etc/apt/
  994  ls
  995  grep -r ansible-runner .
  996  vi sources.list.d/ansible.list 
  997  rm -f sources.list.d/ansible.list 
  998  grep -r mc3man .
  999  rm -f ./sources.list.d/mc3man-ubuntu-xerus-media-jammy.list
 1000  grep -r mc3man .
 1001  apt-get update
 1002  cd
 1003  apt-get install kubectl kubeadm kubelet
 1004  service kubelet status
 1005  clera
 1006  clear
 1007  ls
 1008  kubeadm init
 1009  service docker staus
 1010  service docker status
 1011  swapoff -a
 1012  kubeadm init
 1013  swapoff -a
 1014  sed -i '/ swap / s/^\(.*\)$/#\1/g' /etc/fstab
 1015  kubeadm init
 1016  kubeadm init --v=5
 1017  ls -l /var/run/containerd/containerd.sock
 1018  systemctl status containerd
 1019  clear
 1020  ls
 1021  kubeadm init
 1022  cat /etc/docker/daemon.json
 1023  cd /etc/docker/
 1024  ls
 1025  cd -
 1026  ls
 1027  cd /etc/docker/
 1028  ls
 1029  wget https://gist.githubusercontent.com/melozo/6de91558242fb8ca4212e4a73fbddde6/raw/ec268be8fa53100c44fc21e231e553deee16e856/daemon.json
 1030  ls
 1031  chmod 777 daemon.json 
 1032  more daemon.json 
 1033  ls
 1034  cp daemon.json /root/
 1035  ls
 1036  vi daemon.json 
 1037  service docker restart
 1038  journalctl -xeu docker.service
 1039  cd /var/log/
 1040  ls
 1041  cd -
 1042  ls
 1043  vi daemon.json 
 1044  service docker start
 1045  vi daemon.json 
 1046  service docker start
 1047  vi daemon.json 
 1048  rm daemon.json 
 1049  service docker start
 1050  dockerd
 1051  service docker status
 1052  vi daemon.json
 1053  service docker restart
 1054  service docker status
 1055  kubeadm init
 1056  kubeadm init --ignore-preflight-errors=...
 1057  rm /etc/containerd/config.toml
 1058  systemctl restart containerd
 1059  kubeadm init 
 1060  kubeadm init --skip-phases=addon/kube-proxy --pod-network-cidr=10.244.0.0/16 --v=5
 1061  netstat -peanut | 10250
 1062  netstat -peanut | grep 10250
 1063  service stop kubelet
 1064  kill 53374
 1065  kill 6886
 1066  netstat -peanut | grep 6443
 1067  kubeadm destroy
 1068  kubeadm 
 1069  kubeadm kubeadm reset
 1070  kubeadm reset
 1071  rm -f $HOME/.kube/config
 1072  kubeadm init --skip-phases=addon/kube-proxy --pod-network-cidr=10.244.0.0/16 --v=5
 1073  kubectl edit cm coredns -n kube-system
 1074  kubeadm reset
 1075  kubectl get nodes
 1076  init 
 1077  inito
 1078  init 0
 1079  ls
 1080  cd /opt/
 1081  ls
 1082  kubeadm join 192.168.33.10:6443 --token pkbga9.8hbrwzse3d3xkf7n         --discovery-token-ca-cert-hash sha256:96b3f74312c65a055a3df580bb00b3bfda5498c4d23aa28feb92d4a2db85a81d
 1083  swapoff -a
 1084  kubeadm join 192.168.33.10:6443 --token pkbga9.8hbrwzse3d3xkf7n         --discovery-token-ca-cert-hash sha256:96b3f74312c65a055a3df580bb00b3bfda5498c4d23aa28feb92d4a2db85a81d
 1085  kubeadm reset
 1086  rm -rf /var/lib/kubelet
 1087  cd /etc/kubernetes/
 1088  ls
 1089  rm -rf *
 1090  clear
 1091  ls
 1092  cd..
 1093  cd
 1094  kubeadm reset
 1095  service docker restart
 1096  ls -lart
 1097  kubeadm reset
 1098  clear
 1099  apt-get remove --purge kubelet kubectl kubeadm 
 1100  history
 1101  kubeadm join 192.168.33.10:6443 --token pkbga9.8hbrwzse3d3xkf7n         --discovery-token-ca-cert-hash sha256:96b3f74312c65a055a3df580bb00b3bfda5498c4d23aa28feb92d4a2db85a81d
 1102  apt install -y kubeadm=1.25.0-00 kubelet=1.25.0-00 kubectl=1.25.0-00 --allow-downgrades
 1103  swapoff -a
 1104  kubeadm join 192.168.33.10:6443 --token pkbga9.8hbrwzse3d3xkf7n         --discovery-token-ca-cert-hash sha256:96b3f74312c65a055a3df580bb00b3bfda5498c4d23aa28feb92d4a2db85a81d
 1105  cd /etc/systemd/system/kubelet.service.d
 1106  kubeadm reset
 1107  ls
 1108  vi 10-kubeadm.conf 
 1109  systemctl daemon-reload 
 1110  service kubelet restart
 1111  clear
 1112  cd
 1113  kubeadm join 10.0.2.15:6443 --token ia3gpq.6p2tneszq5andyc8         --discovery-token-ca-cert-hash sha256:865777cbd43fee6211fb8200f9f8cab8e13f3c9785bcb7a2b9e9e6eb660e6532
 1114  dpkg -l libcgroup
 1115  sudo apt-get install cgroup-bin
 1116  apt-get install  cgroup-tools
 1117  sudo mount -t cgroup -o none,name=blkio cgroup /sys/fs/cgroup/blkio
 1118  zcat /proc/config.gz | grep CONFIG_BLK_CGROUP
 1119  mount | grep cgroup
 1120  sudo mount -t cgroup -o none,name=blkio cgroup /sys/fs/cgroup/blkio
 1121  sudo systemctl restart kubelet
 1122  kubeadm join 10.0.2.15:6443 --token ia3gpq.6p2tneszq5andyc8         --discovery-token-ca-cert-hash sha256:865777cbd43fee6211fb8200f9f8cab8e13f3c9785bcb7a2b9e9e6eb660e6532
 1123  clear
 1124  kubeadm join 192.168.33.10:6443 --token vqkqtt.cbh45lszmzdn9jh5 --discovery-token-ca-cert-hash sha256:96b3f74312c65a055a3df580bb00b3bfda5498c4d23aa28feb92d4a2db85a81d
 1125  ifconfig
 1126  clear
 1127  ls
 1128  cd birru-build/
 1129  ls
 1130  cd ansible-runner/
 1131  ls
 1132  cd
 1133  cd /opt/
 1134  ls
 1135  cd demo
 1136  ls
 1137  cd demo-runner/
 1138  ls
 1139  cd demo-runner/
 1140  ls
 1141  cd ..
 1142  ls
 1143  cd ..
 1144  ls
 1145  cd ..
 1146  ls
 1147  cd ansible-runner/
 1148  ls
 1149  cd demo/
 1150  ls
 1151  more playbook.yaml 
 1152  ls
 1153  cp -r /opt/one .
 1154  ls
 1155  vi execution-environment.yml 
 1156  pwd
 1157  vi execution-environment.yml 
 1158  history
 1159  ansible-builder build --tag vikaschenny/ee-trianz:v2.0
 1160  vi execution-environment.yml 
 1161  ls
 1162  ansible-builder build --tag vikaschenny/ee-trianz:v2.0
 1163  vi execution-environment.yml 
 1164  ansible-builder build --tag vikaschenny/ee-trianz:v2.0
 1165  vi execution-environment.yml 
 1166  ansible-builder build --tag vikaschenny/ee-trianz:v2.0
 1167  cd one/
 1168  pwd
 1169  cd ..
 1170  vi execution-environment.yml 
 1171  ansible-builder build --tag vikaschenny/ee-trianz:v2.0
 1172  vi execution-environment.yml 
 1173  ls
 1174  cp -r one context/
 1175  cd context
 1176  ls
 1177  cd ..
 1178  ls
 1179  vi execution-environment.yml 
 1180  ansible-builder build --tag vikaschenny/ee-trianz:v2.0
 1181  docker images
 1182  ls
 1183  cd one/
 1184  ls
 1185  ./run_playbook.sh 
 1186  docker ps -a
 1187  docker rm $(docker ps -a -q)
 1188  vi run_playbook.sh 
 1189  docker run  -v /opt/one/${ip}_hosts.ini:/etc/ansible/hosts -it vikaschenny/trianz-ee-demo:v2.0 bash
 1190  docker images
 1191  docker run  -v /opt/one/${ip}_hosts.ini:/etc/ansible/hosts -it vikaschenny/ee-trianz:v2.0 bash
 1192  ls
 1193  clear
 1194  ls
 1195  vi run_playbook.sh 
 1196  ./run_playbook.sh 
 1197  docker images
 1198  vi run_playbook.sh 
 1199  ./run_playbook.sh 
 1200  docker logs -f 7f9c55b922840b891e2aa5087c191493f400a2c1a15889c7a08f09704749156d
 1201  docker logs -f 007ec1844fe1048e816b59acbaf5267b6923e1ad8d9a4b811a032a5ee1726da8
 1202  ifconfig
 1203  ./run_playbook.sh 
 1204  docker logs -f d64726ea82836a7cd1e85784dfad30f7463c2b15dde50b3fccce3d387d4b8bd5
 1205  more run_playbook.sh 
 1206  ls
 1207  docker images
 1208  docker push vikaschenny/ee-trianz:v2.0 
 1209  exit
 1210  ls
 1211  cd /opt/one/
 1212  ls
 1213  more 192.168.33.11_hosts.ini 
 1214  ls
 1215  more 10.0.2.15_hosts.ini 
 1216  docker images
 1217  kubectl get pods --all-namespaces
 1218  cd /etc/systemd/system/kubelet.service.d
 1219  ls
 1220  vi 10-kubeadm.conf 
 1221  systemctl daemon-reload 
 1222  service kubelet restart
 1223  init 6
 1224  ls
 1225  cd demo/
 1226  ls
 1227  cd artifacts/
 1228  ls
 1229  ls -lart
 1230  cd edad081f-0d3a-4890-9200-b720b80d2df5/
 1231  ls
 1232  ls -lart
 1233  vi ssh_key_data 
 1234  ls
 1235  cd /opt/
 1236  ls
 1237  cd one/
 1238  ls
 1239  pwd
 1240  ansible-runner
 1241  apt install python3-ansible-runner
 1242  ansible-runner run /opt/one playbook.yml 
 1243  ansible-runner run /opt/one/ -p playbook.yml 
 1244  ls
 1245  vi hosts
 1246  ansible-runner run /opt/one/ -p playbook.yml -d
 1247  ansible-runner run /opt/one/ -p playbook.yml --inventory hosts
 1248  ls
 1249  cd..
 1250  cd ..
 1251  ls
 1252  cd demo
 1253  cd ..
 1254  ls
 1255  cd ansible-runner/
 1256  ls
 1257  git status
 1258  git remote -v
 1259  git add .
 1260  git commit -m " update data"
 1261  git push
 1262  cd ..
 1263  ls
 1264  cd demo
 1265  ls
 1266  git status
 1267  cd demo-runner/
 1268  git status
 1269  cd
 1270  clear
 1271  cd -
 1272  ls
 1273  ifconfig
 1274  ls
 1275  cd ../..
 1276  ls
 1277  cd one/
 1278  ls
 1279  cp /tmp/my_key.pem 
 1280  cp /tmp/my_key.pem  .
 1281  ls
 1282  clear
 1283  ls
 1284  ssh-keygen -p -f my_key.pem
 1285  ls
 1286  rm -f my_key.pem 
 1287  rm -f /tmp/my_key.pem 
 1288  ls
 1289  cp /tmp/my_key.pem .
 1290  ls
 1291  vi demo_hosts
 1292  pwd
 1293  vi demo_hosts
 1294  ls
 1295  chmod 777 demo_hosts 
 1296  ls
 1297  ansible-runner run /opt/one/ -p playbook.yml --inventory demo_hosts 
 1298  vi demo_hosts 
 1299  ansible-runner run /opt/one/ -p playbook.yml --inventory demo_hosts 
 1300  ansible-runner run /opt/one/ -p playbook.yml --inventory demo_hosts -vvv
 1301  ls
 1302  vi testplay.yaml
 1303  vi demo_hosts 
 1304  cp demo_hosts demo_hosts.bkp
 1305  vi demo_hosts 
 1306  vi testplay.yaml 
 1307  ansible-runner run /opt/one/ -p testplay.yaml --inventory demo_hosts -vvv
 1308  ls
 1309  ssh -i my_key.pem vikas@192.168.33.11
 1310  ssh  vikas@192.168.33.11
 1311  clear
 1312  ansible-runner run /opt/one/ -p testplay.yaml --inventory demo_hosts -vvv
 1313  ls
 1314  vi demo_hosts
 1315  ansible-runner run /opt/one/ -p testplay.yaml --inventory demo_hosts -vvv
 1316  ansible-runner run /opt/one/ -p testplay.yaml --inventory demo_hosts -vvv -k
 1317  ls
 1318  vi demo_hosts
 1319  ansible-runner run /opt/one/ -p testplay.yaml --inventory demo_hosts -vvv -k
 1320  ansible-runner run /opt/one/ -p testplay.yaml --inventory demo_hosts -vvv 
 1321  ls
 1322  vi demo_hosts
 1323  ansible-runner run /opt/one/ -p testplay.yaml --inventory demo_hosts -vvv 
 1324  vi demo_hosts
 1325  ansible-runner run /opt/one/ -p testplay.yaml --inventory demo_hosts -vvv 
 1326  eval "$(ssh-agent)"
 1327  ssh-add /opt/one/my_key.pem
 1328  ansible-runner run /opt/one/ -p testplay.yaml --inventory demo_hosts -vvv 
 1329  ls
 1330  cp demo_hosts demo_hosts.bkp1
 1331  vi demo_hosts
 1332  eval "$(ssh-agent)"
 1333  ssh-add /opt/one/my_key.pem
 1334  ansible-runner run /opt/one/ -p testplay.yaml --inventory demo_hosts -vvv 
 1335  ls
 1336  vi demo_hosts
 1337  more demo_hosts.bkp1
 1338  vi demo_hosts
 1339  more demo_hosts
 1340  clear
 1341  eval "$(ssh-agent)"
 1342  ssh-add /opt/one/my_key.pem 
 1343  ansible-runner run /opt/one/ -p testplay.yaml 
 1344  ansible-runner run /opt/one/ -p testplay.yaml -d
 1345  ansible-runner run /opt/one/ -p testplay.yaml --inventory demo_hosts
 1346  vi /etc/ssh/sshd_config
 1347  cd
 1348  cd .ssh/
 1349  vi config
 1350  cd
 1351  cd /opt/one/
 1352  ls
 1353  ssh-add -l
 1354  ansible-runner run /opt/one/ -p testplay.yaml --inventory demo_hosts
 1355  vi /root/.ssh/config 
 1356  ansible-runner run /opt/one/ -p testplay.yaml --inventory demo_hosts
 1357  vi /root/.ssh/config 
 1358  clear
 1359  eval "$(ssh-agent)"
 1360  ssh-add /opt/one/my_key.pem 
 1361  ssh-add -l
 1362  ansible-runner run /opt/one/ -p testplay.yaml --inventory demo_hosts -vvv
 1363  vi /root/.ssh/config 
 1364  ansible-runner run /opt/one/ -p testplay.yaml --inventory demo_hosts -vvv
 1365  vi /root/.ssh/config 
 1366  ssh-agent bash
 1367  ssh-add /opt/one/my_key.pem
 1368  ansible-runner run /opt/one/ -p testplay.yaml --inventory demo_hosts -vvv
 1369  ls
 1370  vi demo_hosts
 1371  clear
 1372  ansible-runner run /opt/one/ -p testplay.yaml --inventory demo_hosts -vvv
 1373  vi demo_hosts
 1374  ansible-runner run /opt/one/ -p testplay.yaml --inventory demo_hosts -vvv --ask-pass
 1375  ansible-runner run /opt/one/ -p testplay.yaml --inventory demo_hosts -vvv --extra-vars "private_key_pass=vikas"
 1376  ls
 1377  vi testplay.yaml 
 1378  ansible-runner run /opt/one/ -p testplay.yaml --inventory demo_hosts -vvv
 1379  ls
 1380  apt-get install keychain
 1381  ansible-runner run /opt/one/ -p testplay.yaml --inventory demo_hosts -vvv --ask-pass
 1382  clear
 1383  ls
 1384  vi demo_hosts
 1385  ansible-runner run /opt/one/ -p testplay.yaml --inventory demo_hosts -vvv --ask-pass
 1386  ansible-runner run /opt/one/ -p testplay.yaml --inventory demo_hosts -vvv 
 1387  ls
 1388  mkdir env
 1389  ls
 1390  mkdir project 
 1391  cp playbook.yml project/
 1392  cp testplay.yaml project/
 1393  git clone https://github.com/ansible/ansible-runner.git
 1394  cp -r  ansible-runner/demo .
 1395  rm -rf ansible-runner/
 1396  ls
 1397  cd demo/
 1398  ls
 1399  vi project/
 1400  cd project/
 1401  ls
 1402  more test.yml 
 1403  more roles/
 1404  cd roles/
 1405  ls
 1406  cd testrole/
 1407  ls
 1408  cd tasks/
 1409  ls
 1410  more main.yml 
 1411  cd /opt/one/demo/
 1412  ls
 1413  cd env/
 1414  ls
 1415  more extravars 
 1416  more passwords 
 1417  vi passwords 
 1418  more envvars 
 1419  vi passwords 
 1420  ls
 1421  cp ../../my_key.pem .
 1422  ls
 1423  more ssh_key 
 1424  cat my_key.pem > ssh_key 
 1425  ls
 1426  vi ssh_key 
 1427  vi settings 
 1428  cd ..
 1429  ls
 1430  cd inventory/
 1431  ls
 1432  vi hosts 
 1433  cd ..
 1434  ls
 1435  ansible-runner --help
 1436  ls
 1437  cd project/
 1438  ls
 1439  pwd
 1440  cd ..
 1441  ls
 1442  cd inventory/
 1443  ls
 1444  cd ..
 1445  ls
 1446  clear
 1447  ls
 1448  clear
 1449  ansible-runner run /opt/one/demo --project-dir /opt/one/demo -p /opt/one/demo/project/test.yaml --inventory /opt/one/demo/inventory
 1450  ls
 1451  more project/test.yml 
 1452  ansible-runner run /opt/one/demo --project-dir /opt/one/demo -p /opt/one/demo/project/test.yaml --inventory /opt/one/demo/inventory -vvv
 1453  ifconfig
 1454  ls
 1455  cd env/
 1456  ls
 1457  cp /tmp/id_rsa .
 1458  ls
 1459  cat id_rsa > ssh_key 
 1460  more ssh_key 
 1461  cd ..
 1462  ls
 1463  clear
 1464  ansible-runner run /opt/one/demo --project-dir /opt/one/demo -p /opt/one/demo/project/test.yaml --inventory /opt/one/demo/inventory -vvv
 1465  ansible-runner run /opt/one/demo --project-dir /opt/one/demo -p test.yaml --inventory /opt/one/demo/inventory -vvv
 1466  ansible-runner run /opt/one/demo --project-dir /opt/one/demo -p project/test.yml --inventory /opt/one/demo/inventory -vvv
 1467  cd project/
 1468  ls
 1469  ansible-runner run /opt/one/demo --project-dir /opt/one/demo -p test.yaml --inventory /opt/one/demo/inventory -vvv
 1470  ll
 1471  ansible-runner run /opt/one/demo --project-dir /opt/one/demo -p /opt/one/demo/project/test.yml --inventory /opt/one/demo/inventory -vvv
 1472  cd ..
 1473  ansible-runner run /opt/one/demo --project-dir /opt/one/demo -p /opt/one/demo/project/test.yml --inventory /opt/one/demo/inventory -vvv
 1474  ls
 1475  cd env/
 1476  ls
 1477  vi passwords 
 1478  cd ..
 1479  ls
 1480  cd env/
 1481  ls
 1482  cat my_key.pem > ssh_key 
 1483  more ssh_key 
 1484  cd ..
 1485  ls
 1486  ansible-runner run /opt/one/demo --project-dir /opt/one/demo -p /opt/one/demo/project/test.yml --inventory /opt/one/demo/inventory -vvv
 1487  ls
 1488  cd artifacts/
 1489  ls
 1490  ll
 1491  cd edad081f-0d3a-4890-9200-b720b80d2df5
 1492  ls
 1493  cat ssh_key_data 
 1494  cat stderr 
 1495  cat stdout 
 1496  cat status 
 1497  cd job_events/
 1498  ls
 1499  cat 1-fffd574e-0ebc-4163-a32d-8da2f77452af.json 
 1500  cd ..
 1501  ls
 1502  cat ssh_key_data 
 1503  more ssh_key_data 
 1504  cd /opt/one/
 1505  ls
 1506  cd demo/
 1507  ls
 1508  cd artifacts/
 1509  ls
 1510  cd edad081f-0d3a-4890-9200-b720b80d2df5/
 1511  ls
 1512  cd job_events/
 1513  ls
 1514  cat 1-fffd574e-0ebc-4163-a32d-8da2f77452af.json 
 1515  ls
 1516  cd ..
 1517  ls
 1518  cd job_events/
 1519  expect
 1520  apt  install expect
 1521  cd /opt/one/
 1522  ls
 1523  cd demo/
 1524  ansible-runner run /opt/one/demo --project-dir /opt/one/demo -p /opt/one/demo/project/test.yml --inventory /opt/one/demo/inventory -vvv
 1525  ls
 1526  cd env/
 1527  ls
 1528  vi passwords 
 1529  cd ..
 1530  ansible-runner run /opt/one/demo --project-dir /opt/one/demo -p /opt/one/demo/project/test.yml --inventory /opt/one/demo/inventory -vvv
 1531  cd ..
 1532  ls
 1533  cd -
 1534  ls
 1535  cd artifacts/aeabe956-f05a-4640-9433-a1c8cd7e1cae/
 1536  ls
 1537  cd job_events/
 1538  ls
 1539  cd -
 1540  cd ..
 1541  ls
 1542  ls -lart
 1543  cd 39ef0781-2b98-4834-9883-078cf96a57da/
 1544  ls
 1545  cd job_events/
 1546  ls
 1547  cat 1-d24e8ff4-2d08-41f1-a7f9-b0fc59a65471.json 
 1548  cd /opt/one/demo/env/
 1549  ls
 1550  vi passwords 
 1551  cd ..
 1552  ansible-runner run /opt/one/demo --project-dir /opt/one/demo -p /opt/one/demo/project/test.yml --inventory /opt/one/demo/inventory -vvv
 1553  apt-get remove expect
 1554  ansible-runner run /opt/one/demo --project-dir /opt/one/demo -p /opt/one/demo/project/test.yml --inventory /opt/one/demo/inventory -vvv
 1555  ls
 1556  cd env/
 1557  ls
 1558  cd ..
 1559  ls
 1560  cd env/ls
 1561  cd env/
 1562  ls
 1563  more ssh_key 
 1564  ls
 1565  cd ..
 1566  ls
 1567  cd inventory/
 1568  ls
 1569  ifconfig
 1570  ls
 1571  vi hosts 
 1572  ls
 1573  cd ..
 1574  ls
 1575  more inventory/hosts 
 1576  s
 1577  l
 1578  cd env/
 1579  ls
 1580  pwd
 1581  ls
 1582  cd ..
 1583  ls
 1584  cd inventory/
 1585  ls
 1586  cp hosts hosts_bkp.txt
 1587  vi hosts
 1588  cd ..
 1589  ls
 1590  cd env/
 1591  ls
 1592  cd ..
 1593  ls
 1594  cd ..
 1595  ls
 1596  git remote -v
 1597  git init 
 1598  history > commands.md
