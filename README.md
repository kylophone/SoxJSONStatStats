SoxJSONStatStats
====

Personal fork of the stat and stats effects in <a href = "http://sox.sourceforge.net/"> SOX</a>. Provides an additional option for JSON output. If you're tired of parsing the output of SOX and would rather use JSON, compile SOX with these two files. The 'stats' effect is generally more useful, and provides information about each channel in a multi-channel file. To use, just add a '-json' flag after you call stat or stats, like this: 

```bash
$ sox somefile.wav -n stat -json

{
	"samplesRead" : 657090,
	"lengthInSeconds" : 14.900000,
	"scaledBy" : 2147483647.000000,
	"maximumAmplitude" : 0.434052,
	"minimumAmplitude" : -0.528595,
	"midlineAmplitude" : -0.047272,
	"meanNorm" : 0.044004,
	"meanAmplitude" : -0.000000,
	"RMSAmplitude" : 0.074119,
	"maximumDelta" : 0.171356,
	"minimumDelta" : 0.000000,
	"meanDelta" : 0.004453,
	"RMSDelta" : 0.009420,
	"roughFrequency" : 891,
	"volumeAdjustment" : 1.891808
}
```
OR
```bash
$ sox somefile.wav -n stats -json

{
"channelCount" : 4,
"overall" : {
	"dcOffset" : 0.000979,
	"minLevel" : -0.969940,
	"maxLevel" : 0.794006,
	"peakLeveldB" : -0.265101,
	"RMSLeveldB" : -25.984172,
	"RMSPeakdB" : -11.744568,
	"RMSTrdB" : -inf,
	"crestFactor" : "-",
	"flatFactor" : 0.000000,
	"pkCount" : 2,
	"bitDepth" : "16/16",
	"numSamples" : 169,
	"lengthSeconds" : 3.832902,
	"scaleMax" : 1.0,
	"windowSeconds" : 0.050000,
	},
"ch1" : {
	"dcOffset" : 0.000400,
	"minLevel" : -0.312927,
	"maxLevel" : 0.679260,
	"peakLeveldB" : -3.359276,
	"RMSLeveldB" : -27.832778,
	"RMSPeakdB" : -14.554000,
	"RMSTrdB" : -309.033158,
	"crestFactor" : 16.736902,
	"flatFactor" : 0.000000,
	"pkCount" : 2,
	"bitDepth" : "15/16",
	},
"ch2" : {
	"dcOffset" : 0.000569,
	"minLevel" : -0.368256,
	"maxLevel" : 0.678070,
	"peakLeveldB" : -3.374509,
	"RMSLeveldB" : -28.717487,
	"RMSPeakdB" : -15.859836,
	"RMSTrdB" : -inf,
	"crestFactor" : 18.499029,
	"flatFactor" : 0.000000,
	"pkCount" : 2,
	"bitDepth" : "15/16",
	},
"ch3" : {
	"dcOffset" : 0.000979,
	"minLevel" : -0.576294,
	"maxLevel" : 0.794006,
	"peakLeveldB" : -2.003521,
	"RMSLeveldB" : -24.530456,
	"RMSPeakdB" : -12.576707,
	"RMSTrdB" : -inf,
	"crestFactor" : 13.376631,
	"flatFactor" : 0.000000,
	"pkCount" : 2,
	"bitDepth" : "16/16",
	},
"ch4" : {
	"dcOffset" : -0.000176,
	"minLevel" : -0.969940,
	"maxLevel" : 0.585571,
	"peakLeveldB" : -0.265101,
	"RMSLeveldB" : -24.473025,
	"RMSPeakdB" : -11.744568,
	"RMSTrdB" : -inf,
	"crestFactor" : 16.232903,
	"flatFactor" : 0.000000,
	"pkCount" : 2,
	"bitDepth" : "16/16",
	},
}
```

