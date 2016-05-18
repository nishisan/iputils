#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_PREREQ([2.63])
AC_INIT([iputils], [0.1], [lucas.nishimura@gmail.com])
AM_INIT_AUTOMAKE(pingd, 0.1)
AC_CONFIG_SRCDIR([src/ping.c])
AC_CONFIG_HEADERS([config.h])

AC_CONFIG_MACRO_DIR([libltdl/m4])
LT_CONFIG_LTDL_DIR([libltdl])
LT_INIT([dlopen])
LTDL_INIT([recursive])

# Checks for programs.
#AC_PROG_CC

# Checks for libraries.
# FIXME: Replace `main' with a function in `-lcap':
AC_CHECK_LIB([cap], [main])
# FIXME: Replace `main' with a function in `-lcrypto':
AC_CHECK_LIB([crypto], [main])
# FIXME: Replace `main' with a function in `-lgcrypt':
AC_CHECK_LIB([gcrypt], [main])
# FIXME: Replace `main' with a function in `-lidn':
AC_CHECK_LIB([idn], [main])
# FIXME: Replace `main' with a function in `-lm':
AC_CHECK_LIB([m], [main])
# FIXME: Replace `main' with a function in `-lnettle':
AC_CHECK_LIB([nettle], [main])
# FIXME: Replace `main' with a function in `-lresolv':
AC_CHECK_LIB([resolv], [main])
# FIXME: Replace `main' with a function in `-lrt':
AC_CHECK_LIB([rt], [main])
# FIXME: Replace `main' with a function in `-lsysfs':
AC_CHECK_LIB([sysfs], [main])

# Checks for header files.
AC_HEADER_RESOLV
AC_CHECK_HEADERS([arpa/inet.h fcntl.h limits.h locale.h malloc.h netdb.h netinet/in.h stdlib.h string.h sys/file.h sys/ioctl.h sys/param.h sys/socket.h sys/time.h syslog.h unistd.h])

# Checks for typedefs, structures, and compiler characteristics.
AC_C_INLINE
AC_TYPE_OFF_T
AC_TYPE_PID_T
AC_TYPE_SIZE_T
AC_TYPE_SSIZE_T
AC_TYPE_UID_T
AC_TYPE_UINT16_T
AC_TYPE_UINT32_T

# Checks for library functions.
AC_FUNC_FORK
AC_FUNC_MALLOC
AC_FUNC_STRTOD
AC_CHECK_FUNCS([alarm clock_gettime dup2 gethostbyname gethostname gettimeofday inet_ntoa memchr memset select setlocale socket strchr strdup strerror strtol strtoul])

AC_CONFIG_FILES([src/lib/Makefile
 		 Makefile
                 src/Makefile])
AC_CONFIG_SUBDIRS([lib/libconfig
                   src/ninfod])
AC_OUTPUT
