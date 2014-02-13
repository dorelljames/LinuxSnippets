#!/bin/bash

lang='en'

localedef --list-archive | grep -v -i ^$lang | xargs localedef --delete-from-archive
