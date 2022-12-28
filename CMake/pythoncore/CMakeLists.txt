PROJECT( pythoncore C )

CMAKE_MINIMUM_REQUIRED( VERSION 2.8 )

SET( pythoncore_headers
    ../../Include/abstract.h
    ../../Include/accu.h
    ../../Include/asdl.h
    ../../Include/ast.h
    ../../Include/bitset.h
    ../../Include/boolobject.h
    ../../Include/bytes_methods.h
    ../../Include/bytearrayobject.h
    ../../Include/bytesobject.h
    ../../Include/cellobject.h
    ../../Include/ceval.h
    ../../Include/classobject.h
    ../../Include/code.h
    ../../Include/codecs.h
    ../../Include/compile.h
    ../../Include/complexobject.h
    ../../Include/datetime.h
    ../../Include/descrobject.h
    ../../Include/dictobject.h
    ../../Include/dynamic_annotations.h
    ../../Include/enumobject.h
    ../../Include/errcode.h
    ../../Include/eval.h
    ../../Include/fileobject.h
    ../../Include/fileutils.h
    ../../Include/floatobject.h
    ../../Include/frameobject.h
    ../../Include/funcobject.h
    ../../Include/genobject.h
    ../../Include/graminit.h
    ../../Include/grammar.h
    ../../Include/import.h
    ../../Include/intrcheck.h
    ../../Include/iterobject.h
    ../../Include/listobject.h
    ../../Include/longintrepr.h
    ../../Include/longobject.h
    ../../Include/marshal.h
    ../../Include/memoryobject.h
    ../../Include/metagrammar.h
    ../../Include/methodobject.h
    ../../Include/modsupport.h
    ../../Include/moduleobject.h
    ../../Include/namespaceobject.h
    ../../Include/node.h
    ../../Include/object.h
    ../../Include/objimpl.h
    ../../Include/opcode.h
    ../../Include/osdefs.h
    ../../Include/parsetok.h
    ../../Include/patchlevel.h
    ../../Include/pgen.h
    ../../Include/pgenheaders.h
    ../../Include/pyhash.h
    ../../Include/py_curses.h
    ../../Include/pyarena.h
    ../../Include/pycapsule.h
    ../../Include/pyctype.h
    ../../Include/pydebug.h
    ../../Include/pyerrors.h
    ../../Include/pyexpat.h
    ../../Include/pyfpe.h
    ../../Include/pygetopt.h
    ../../Include/pymath.h
    ../../Include/pytime.h
    ../../Include/pymacro.h
    ../../Include/pymem.h
    ../../Include/pyport.h
    ../../Include/pystate.h
    ../../Include/pystrcmp.h
    ../../Include/pystrtod.h
    ../../Include/dtoa.h
    ../../Include/Python-ast.h
    ../../Include/Python.h
    ../../Include/pythonrun.h
    ../../Include/pythread.h
    ../../Include/rangeobject.h
    ../../Include/setobject.h
    ../../Include/sliceobject.h
    ../../Include/structmember.h
    ../../Include/structseq.h
    ../../Include/symtable.h
    ../../Include/sysmodule.h
    ../../Include/token.h
    ../../Include/traceback.h
    ../../Include/tupleobject.h
    ../../Include/ucnhash.h
    ../../Include/unicodeobject.h
    ../../Include/weakrefobject.h
    ../../Modules/_math.h
    ../../Modules/hashtable.h
    ../../Modules/rotatingtree.h
    ../../Modules/sre.h
    ../../Modules/sre_constants.h
    ../../Modules/sre_lib.h
    ../../Modules/_io/_iomodule.h
    ../../Modules/cjkcodecs/alg_jisx0201.h
    ../../Modules/cjkcodecs/cjkcodecs.h
    ../../Modules/cjkcodecs/emu_jisx0213_2000.h
    ../../Modules/cjkcodecs/mappings_cn.h
    ../../Modules/cjkcodecs/mappings_hk.h
    ../../Modules/cjkcodecs/mappings_jisx0213_pair.h
    ../../Modules/cjkcodecs/mappings_jp.h
    ../../Modules/cjkcodecs/mappings_kr.h
    ../../Modules/cjkcodecs/mappings_tw.h
    ../../Modules/cjkcodecs/multibytecodec.h
    ../../Objects/stringlib/count.h
    ../../Objects/stringlib/fastsearch.h
    ../../Objects/stringlib/find.h
    ../../Objects/stringlib/partition.h
    ../../Objects/stringlib/replace.h
    ../../Objects/stringlib/split.h
    ../../Objects/unicodetype_db.h
    ../../Parser/parser.h
    ../../Parser/tokenizer.h
    ../../Python/ceval_gil.h
    ../../Python/condvar.h
    ../../Python/importdl.h
    ../../Python/thread_nt.h )

IF(CMAKE_GENERATOR MATCHES Visual*)
    SET( pythoncore_headers
		${pythoncore_headers}
		../../Windows/errmap.h
		../../Windows/pyconfig.h )
ENDIF()


SET( pythoncore_sources
    ../../Modules/getbuildinfo.c
    ../../Modules/_bisectmodule.c
    ../../Modules/_codecsmodule.c
    ../../Modules/_collectionsmodule.c
    ../../Modules/_csv.c
    ../../Modules/_functoolsmodule.c
    ../../Modules/_heapqmodule.c
    ../../Modules/_json.c
    ../../Modules/_localemodule.c
    ../../Modules/_lsprof.c
    ../../Modules/_math.c
    ../../Modules/_pickle.c
    ../../Modules/_randommodule.c
    ../../Modules/_sre.c
    ../../Modules/_stat.c
    ../../Modules/_struct.c
    ../../Modules/_weakref.c
    ../../Modules/arraymodule.c
    ../../Modules/atexitmodule.c
    ../../Modules/audioop.c
    ../../Modules/binascii.c
    ../../Modules/cmathmodule.c
    ../../Modules/_datetimemodule.c
    ../../Modules/errnomodule.c
    ../../Modules/faulthandler.c
    ../../Modules/gcmodule.c
    ../../Modules/hashtable.c
    ../../Modules/itertoolsmodule.c
    ../../Modules/main.c
    ../../Modules/mathmodule.c
    ../../Modules/md5module.c
    ../../Modules/mmapmodule.c
    ../../Modules/_opcode.c
    ../../Modules/_operator.c
    ../../Modules/parsermodule.c
    ../../Modules/posixmodule.c
    ../../Modules/rotatingtree.c
    ../../Modules/sha1module.c
    ../../Modules/sha256module.c
    ../../Modules/sha512module.c
    ../../Modules/signalmodule.c
    ../../Modules/symtablemodule.c
    ../../Modules/_threadmodule.c
    ../../Modules/_tracemalloc.c
    ../../Modules/timemodule.c
    ../../Modules/xxsubtype.c
    ../../Modules/_io/fileio.c
    ../../Modules/_io/bytesio.c
    ../../Modules/_io/stringio.c
    ../../Modules/_io/bufferedio.c
    ../../Modules/_io/iobase.c
    ../../Modules/_io/textio.c
    ../../Modules/_io/_iomodule.c
    ../../Modules/cjkcodecs/_codecs_cn.c
    ../../Modules/cjkcodecs/_codecs_hk.c
    ../../Modules/cjkcodecs/_codecs_iso2022.c
    ../../Modules/cjkcodecs/_codecs_jp.c
    ../../Modules/cjkcodecs/_codecs_kr.c
    ../../Modules/cjkcodecs/_codecs_tw.c
    ../../Modules/cjkcodecs/multibytecodec.c
    ../../Objects/abstract.c
    ../../Objects/accu.c
    ../../Objects/boolobject.c
    ../../Objects/bytes_methods.c
    ../../Objects/bytearrayobject.c
    ../../Objects/bytesobject.c
    ../../Objects/capsule.c
    ../../Objects/cellobject.c
    ../../Objects/classobject.c
    ../../Objects/codeobject.c
    ../../Objects/complexobject.c
    ../../Objects/descrobject.c
    ../../Objects/dictobject.c
    ../../Objects/enumobject.c
    ../../Objects/exceptions.c
    ../../Objects/fileobject.c
    ../../Objects/floatobject.c
    ../../Objects/frameobject.c
    ../../Objects/funcobject.c
    ../../Objects/genobject.c
    ../../Objects/iterobject.c
    ../../Objects/listobject.c
    ../../Objects/longobject.c
    ../../Objects/memoryobject.c
    ../../Objects/methodobject.c
    ../../Objects/moduleobject.c
    ../../Objects/namespaceobject.c
    ../../Objects/object.c
    ../../Objects/obmalloc.c
    ../../Objects/rangeobject.c
    ../../Objects/setobject.c
    ../../Objects/sliceobject.c
    ../../Objects/structseq.c
    ../../Objects/tupleobject.c
    ../../Objects/typeobject.c
    ../../Objects/unicodectype.c
    ../../Objects/unicodeobject.c
    ../../Objects/weakrefobject.c
    ../../Parser/acceler.c
    ../../Parser/bitset.c
    ../../Parser/firstsets.c
    ../../Parser/grammar.c
    ../../Parser/grammar1.c
    ../../Parser/listnode.c
    ../../Parser/metagrammar.c
    ../../Parser/myreadline.c
    ../../Parser/node.c
    ../../Parser/parser.c
    ../../Parser/parsetok.c
    ../../Parser/tokenizer.c
    ../../Python/pyhash.c
    ../../Python/random.c
    ../../Python/_warnings.c
    ../../Python/asdl.c
    ../../Python/ast.c
    ../../Python/bltinmodule.c
    ../../Python/ceval.c
    ../../Python/codecs.c
    ../../Python/compile.c
    ../../Python/dynamic_annotations.c
    ../../Python/errors.c
    ../../Python/fileutils.c
    ../../Python/formatter_unicode.c
    ../../Python/frozen.c
    ../../Python/future.c
    ../../Python/getargs.c
    ../../Python/getcompiler.c
    ../../Python/getcopyright.c
    ../../Python/getopt.c
    ../../Python/getplatform.c
    ../../Python/getversion.c
    ../../Python/graminit.c
    ../../Python/import.c
    ../../Python/importdl.c
    ../../Python/marshal.c
    ../../Python/modsupport.c
    ../../Python/mysnprintf.c
    ../../Python/mystrtoul.c
    ../../Python/peephole.c
    ../../Python/pyarena.c
    ../../Python/pyctype.c
    ../../Python/pyfpe.c
    ../../Python/pymath.c
    ../../Python/pytime.c
    ../../Python/pystate.c
    ../../Python/pystrcmp.c
    ../../Python/pystrtod.c
    ../../Python/dtoa.c
    ../../Python/Python-ast.c
    ../../Python/pythonrun.c
    ../../Python/structmember.c
    ../../Python/symtable.c
    ../../Python/sysmodule.c
    ../../Python/thread.c
    ../../Python/traceback.c )

IF(CMAKE_GENERATOR MATCHES Visual*)
    SET( pythoncore_sources
	${pythoncore_sources}
	../../Windows/winreg.c
    ../../Windows/config.c
    ../../Windows/dl_nt.c
    ../../Windows/getpathp.c
    ../../Windows/msvcrtmodule.c
    ../../Modules/_winapi.c
    ../../Python/dynload_win.c)
ELSE()
    SET( pythoncore_sources
	${pythoncore_sources}
	../../Linux/config.c
    ../../Modules/getpath.c
    ../../Modules/pwdmodule.c
    ../../Modules/_posixsubprocess.c
    ../../Modules/selectmodule.c
    ../../Python/dynload_shlib.c )
ENDIF()

IF(CMAKE_GENERATOR MATCHES Visual*)
    INCLUDE_DIRECTORIES( ../../Windows )
ELSE()
    INCLUDE_DIRECTORIES( ../../Linux )
ENDIF()

INCLUDE_DIRECTORIES( ../../Include )

ADD_DEFINITIONS( -D_USRDLL -DPy_BUILD_CORE -DPy_ENABLE_SHARED -DSOABI=\"cpython-34m\" -DPREFIX=\".\" -DEXEC_PREFIX=\".\" -DVERSION=\"3.4\" -DVPATH=\"\")

IF(CMAKE_GENERATOR MATCHES Visual*)
    ADD_DEFINITIONS( -DWIN32 )
ENDIF()

ADD_LIBRARY( python34 SHARED ${pythoncore_sources} ${pythoncore_headers} )
INSTALL( TARGETS python34 DESTINATION ${INSTALL_DESTINATION} )
