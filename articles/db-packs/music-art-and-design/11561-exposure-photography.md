# Exposure (photography)

In photography, exposure is the amount of light per unit area reaching a frame of photographic film or the surface of an electronic image sensor. It is determined by exposure time, lens f-number (the aperture setting), and scene luminance, and is measured in lux-seconds (lx·s). An "exposure" also names a single shutter cycle: a long exposure means one long shutter opening, while a multiple exposure layers several shutter cycles into one image. Total accumulated light depends only on the sum of exposure times.

## How exposure is defined formally

Two parallel definitions exist. Radiant exposure of a surface, written $H_e$ (the "e" marks it as energetic), uses radiometric units and is measured in joules per square metre:

$$H_e = E_e \, t$$

where $E_e$ is irradiance in W/m² and $t$ is exposure duration in seconds. Luminous exposure, $H_v$ (the "v" marks it as visual), uses photometric units (light weighted by the eye's sensitivity) and is measured in lux-seconds:

$$H_v = E_v \, t$$

where $E_v$ is illuminance in lux. Both quantities are time-integrated illuminance or irradiance. Only when the measurement is weighted by the actual spectral sensitivity of the photosensitive surface does $H$ describe the light that actually reacts with the film. This is why a characteristic curve (the film's plot of light received versus density produced) remains valid regardless of the light spectrum. Because many photographic materials respond to ultraviolet and infrared as well as visible light, radiometric units are appropriate when that extra sensitivity matters.

In sensitometric data such as characteristic curves, log exposure is conventionally $\log_{10}(H)$. Photographers who think in stops and exposure values convert with $\log_2(H) \approx 3.32 \log_{10}(H)$.

## Optimum exposure and dynamic range

"Correct" exposure is whatever produces the intended image. Technically, every film or sensor has a useful exposure range, sometimes called its dynamic range. If light reaching any part of the photograph falls outside that range, the medium cannot record it accurately: underexposed areas collapse to black, overexposed areas collapse to white. Exposure and lighting adjustments map the scene's significant shadows and highlights into that range so no important detail is lost. Photographers may also deliberately over- or underexpose to suppress unwanted detail, for instance rendering a white cloth immaculate, though it is far easier to discard recorded information in post-processing than to recreate information that was never captured.

When a scene's highlight-to-shadow luminance ratio exceeds the medium's exposure range, no single exposure can keep both ends intact, because exposure adjustments apply to the whole frame. Common fixes are fill lighting in the shadows, a graduated neutral-density filter or scrim over the highlights, or exposure bracketing (shooting the same scene at several exposures) combined in an HDR (high dynamic range) process.

A photograph is overexposed when important bright areas wash out ("blown-out highlights" or "clipped whites") and underexposed when important dark areas turn muddy black ("blocked-up", "crushed", or "clipped" blacks). These are technical descriptors, not aesthetic judgments. Shifting the histogram (the chart of how many pixels have each brightness) toward the right or left by intentional over- or underexposure is called "exposing to the right" or "exposing to the left".

## How photographers control exposure

In manual mode, the photographer sets aperture and shutter speed. Opening the aperture lets in more light but reduces depth of field; slowing the shutter lets in more light but increases motion blur. Automatic exposure modes use an internal meter that targets a mid-tone (a medium grey). Aperture priority (A or Av) lets the photographer set the aperture while the camera chooses the shutter speed; shutter priority (S or Tv) reverses the roles. Exposure compensation, usually calibrated in stops (each stop doubles or halves the light) or EV units, offsets the camera's meter reading: +1 EV doubles the light, −1 EV halves it. This is especially useful with auto-exposure when the meter's assumptions about the scene are wrong.

Medium sensitivity is given as ISO film speed; higher ISO needs less light. Total exposure depends on shutter time, lens aperture, and scene luminance: slower shutter, wider aperture, and a brighter scene all raise it. The sunny 16 rule summarises a baseline: on a sunny day with ISO 100 film, f/16 pairs with a shutter speed of roughly 1/100 s, because the shutter approximates the reciprocal of the ISO.

## Reciprocity and its limits

Reciprocity says the same total exposure can be reached by trading time against aperture: halving the shutter time requires opening the aperture by one stop to admit twice as much light per second. To use f/5.6 instead of f/16 in a sunny-16 scene, three stops wider, the shutter must go from 1/125 s to 1/1000 s.

This trade only holds within roughly 1 s to 1/1000 s. Outside that window, film emulsions lose their linear response and need extra exposure to compensate, a behaviour called reciprocity failure whose size depends on the specific emulsion. Digital sensors can show analogous deviations. The Zone System extends exposure and development choices to fit a wider range of scene contrast than a single standard exposure can capture; digital cameras can reach comparable high dynamic range by combining several bracketed exposures in software.

Latitude is the degree by which an image can be over- or underexposed and still recover acceptable quality. Negative film tolerates overexposure in the highlights well; digital sensors tolerate underexposure in the shadows well but lose highlight detail quickly. Slide film has narrow latitude on both ends. Negative film's latitude grows somewhat with higher ISO; digital's narrows. Recording in a raw image format, or choosing a sensor with greater latitude, can recover some blown highlights after the fact, and film frequently retains recoverable detail through extreme highlights that digital would clip.
