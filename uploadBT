#!/bin/bash

compDir=YS-ev3rt-hrp2
appName=Sample

rm ~/EV3RT/$compDir/sdk/workspace/app
rm -rf ~/EV3RT/$compDir/sdk/workspace/project

cp -r . ~/EV3RT/$compDir/sdk/workspace/project

path=`pwd`

cd ~/EV3RT/$compDir/sdk/workspace/project
mv -v ./Sources/* ./
mv -v ./Headers/* ./
mv -v ./ConfigFiles/* ./
cd ../
make app=project
make upload ip=10.0.10.1 from=app to=$appName
cd $path

cp -r ~/EV3RT/$compDir/sdk/workspace/app .
mv app $appName

rm ~/EV3RT/$compDir/sdk/workspace/app
rm -rf ~/EV3RT/$compDir/sdk/workspace/project
