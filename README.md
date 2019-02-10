# fiomark
crystal mark analog with fio

require:

                fio https://bluestop.org/fio/
                
                jq https://stedolan.github.io/jq/download/ (rename to jq.exe, and story near fiomark script)
                
                bash https://sourceforge.net/projects/win-bash/files/win-bash/0.6/ (rename to bash.exe, and story near fiomark script)
                
using:

linux

                ./fiomark direct libaio /test_path

macosx

                ./fiomark derect /test_path

windows

                ./fiomark direct windowsaio /test_path (but /test_path is broken in my fio, you can copy script to test directory)

                ./fiomark parse - show saved result (it saved to $HOME/.fiomark*)

example:

        I:\fiomark>bash fiomark windowsaio direct
        windowsaio direct 1024m loop=3 .
        Running...
                                 Read [MB/s] Write [MB/s]
                1m      Q32T1       2844.444     2292.537
                         iops         2777.8       2238.8

                4k      Q8T8         650.146      666.898
                         iops       162537.3     166725.3

                4k      Q32T1        403.149      317.355
                         iops       100787.4      79338.8

                4k      Q1T1         191.282      175.342
                         iops        47820.7      43835.6
