#!/bin/bash
for file in $@
do
	ln -s $file `echo $file | sed "s/\//_/g" | sed "s/\._//"`
done

