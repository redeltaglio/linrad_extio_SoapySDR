# linrad_extio_SoapySDR
extio glue allows to use SoapySDR with linrad. linux only. RX only.

only the absolute minimum is implemented

plus setting frequency and gain (just barely) in linrad.
SDR must support CS16 sample type.
samplerate is hardcoded at 8Msps in the source - go find it!
but you can set a device specifier in environment variable LINRAD_SOAPY_DEV - same as what SoapySDRUtil --probe and co takes.

new: _always_ set LINRAD_SOAPY_DEV='driver=something' is you have SoapyRemote installed, otherwise the stream will go thru the embedded SoapyServer and that's slow.

probably dies if the proper standalone SoapyServer is also running.
