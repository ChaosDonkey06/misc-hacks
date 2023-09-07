# Install Dropbox Server

Last used on 2021

# Download
cd ~ && wget -O - "https://www.dropbox.com/download?plat=lnx.x86_64" | tar xzf -

# If dropbox has a lot of files
echo fs.inotify.max_user_watches=1000000 | sudo tee -a /etc/sysctl.conf; sudo sysctl -p

# Probably missing packages
sudo apt-get install -y libglapi-mesa
sudo apt-get install -y libxdamage-dev
sudo apt-get install -y libxcb-glx0
sudo apt-get install libxcb-dri2-0
sudo apt-get install -y libxcb-dri3-0
sudo apt-get install -y libxcb-present-dev
sudo apt-get install -y libxshmfence-dev
sudo apt-get install -y libxxf86vm-dev


# Install Deamon
~/.dropbox-dist/dropboxd

# Install CLI (must have python)
sudo wget -O /usr/local/bin/dropbox "https://www.dropbox.com/download?dl=packages/dropbox.py"
sudo chmod +x /usr/local/bin/dropbox



# Exclude a lot of files
dropbox exclude add AWS
dropbox exclude add Andres
dropbox exclude add BackUps
dropbox exclude add Camera\ Uploads
dropbox exclude add Compartidas
dropbox exclude add Cotizaciones
dropbox exclude add Cuentas\ de\ Cobro
dropbox exclude add Deudas
dropbox exclude add GIS
dropbox exclude add Gina
dropbox exclude add Gonzalez-Casabianca
dropbox exclude add Learn
dropbox exclude add Legacy
dropbox exclude add Libros
dropbox exclude add M
dropbox exclude add Movies
dropbox exclude add Personal
dropbox exclude add Procesos\ de\ Aplicacion
dropbox exclude add Projects/ABM
dropbox exclude add Projects/Andres\ Angel\ -\ Felipe\ Gonzalez\ -\ Juan\ Felipe\ Ceron\ -Paula\ Rodriguez-Julian\ Chitiva
dropbox exclude add Projects/Andres\ Angel-Alejandro\ Feged-Felipe\ Gonzalez
dropbox exclude add Projects/Andres_Angel-Felipe_Fongalez
dropbox exclude add Projects/CAOBA
dropbox exclude add Projects/CRBM
dropbox exclude add Projects/CS229
dropbox exclude add Projects/Citas\ Rosario
dropbox exclude add Projects/Cyclo-Octano
dropbox exclude add Projects/DatosDC
dropbox exclude add Projects/FINAL_Jsons_AGI
dropbox exclude add Projects/Gina
dropbox exclude add Projects/Guapi
dropbox exclude add Projects/Guapi\ Paper\ Feb_2019
dropbox exclude add Projects/Jaime
dropbox exclude add Projects/Malaria-GEE
dropbox exclude add Projects/Malaria-Guapi
dropbox exclude add Projects/Malaria_Guapi_EquipoCol
dropbox exclude add Projects/MinTIC\ -\ Termometro
dropbox exclude add Projects/Proyecto\ Datos\ Tracking\ de\ Futbol
dropbox exclude add Projects/Quantil
dropbox exclude add Projects/a-VPH-TDA
dropbox exclude add Projects/a-urban_malaria
dropbox exclude add Projects/a.diplomado
dropbox exclude add Projects/corona_virus
dropbox exclude add Projects/disease_powerlaws
dropbox exclude add Projects/lau_go
dropbox exclude add Projects/manuela
dropbox exclude add Projects/pMSC
dropbox exclude add Projects/scalability_disease
dropbox exclude add Projects/vinco
dropbox exclude add Projects/covid_fb_pipeline
dropbox exclude add Projects/quick-wrinkle
dropbox exclude add Projects/bioinformatics_uc_san_diego
dropbox exclude add Projects/covid_amazonas
dropbox exclude add Projects/covid_bogota_proceso_muestras
dropbox exclude add Projects/covid_grafos
dropbox exclude add Projects/covid_jaime
dropbox exclude add Projects/Draft_Amazonas_2020-08-26
dropbox exclude add Projects/katz-bonacich
dropbox exclude add Projects/mapperKD
dropbox exclude add Projects/mapperKD_old
dropbox exclude add Projects/shape_files
dropbox exclude add Projects/subtitle_translator
dropbox exclude add Projects/datalama-grants
dropbox exclude add Triglav
dropbox exclude add Universidad
dropbox exclude add connections
dropbox exclude add enviorments
dropbox exclude add figures_for_paper
dropbox exclude add new_film
dropbox exclude add recsys
dropbox exclude add roca_solida



