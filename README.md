# TARGETS

Simple parallel perl build system. Can be simply modified for several uses.

Normaly build file is named `TARGETS` and contains some make-style build process description:

~~~~~
# exaple target file

target foo,
depends ('bar'),
imply {
  # do some stuff...
  return 0;
};

target clean,
imply {
	`rm -f *.o`;
	return 0;
};
~~~~~
