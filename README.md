# Monitoring COVID Patients at Home

“It has turned out that six out of seven patients with corona infection can be treated on an _outpatient_ basis – so the hospitals can concentrate on the _more serious cases_”, recently the German Minister of Health, Jens Spahn, said. 

About eighty percent of these _outpatients_ will experience a mild course of the disease, many might even not be aware that they had the virus. But there is also a significant number of patients who will make a very unpleasant acquaintance with the virus. The transition from a mild to an acute live threatening situation can occur fast. A seemingly well doing patient can become within hours one these _more serious cases_ that need to be hospitalised.

Pneumonia is one of the serious complications related to Covid-19. Recent reports seem to indicate that _Covid-19 pneumonia_ shows unusual symptoms. In _New York Times(4/20/20)_, emergency room doctor 
[Richard Levitan](https://en.wikipedia.org/wiki/Richard_Levitan),
speaks about “silent hypoxia” — “silent because of its insidious, hard-to-detect nature”. Patients with such a kind of hypoxia often do not report any sensation of breathing problems, even though their chest X-rays already shows diffuse pneumonia, and their oxygen is below normal. These patients must be treated urgently in hospital, “otherwise they might go on to a second and deadlier phase of lung injury”.

An early and seemingly reliable warning sign that a patient is about to develop _Covid-19 pneumonia_, is his low saturation of blood oxygen. In hospital, blood oxygen is measured with a device called _pulse oximeter_. By providing the patients at home with _pulse oximeters_ we can save the lives of many outpatients just by alerting them or their cohabitants early on the need of intensive treatment.

Richard Levitan says:
> All patients who have been tested positive for the coronavirus should have pulse oximetry monitoring for two weeks, the period during which _Covid pneumonia_ typically develops. All persons with cough, fatigue and fevers should also have _pulse oximeter_ monitoring even if they have not had virus testing, or even if their swab test was negative, because those tests are only about 70 percent accurate. 

See also:
[Levitan, Richard (20 April 2020). "The Infection That's Silently Killing Coronavirus Patients". The New York Times.](https://www.nytimes.com/2020/04/20/opinion/coronavirus-testing-pneumonia.html)

## Using a Smart Watch in Place of the Pulse Oximeter

Unfortunately, _simple pulse oximeters_ for use at home are currently sold out. 

Alternatively there are a number _smart watches_ that have build-in _pulse oximeter_. At first sight it might seem exaggerated to use such a sophisticated technology for just measuring something as simple as blood oxidation.

But at a second glance, using the _smart-watch_ in combination with a _smart-phone_ has many attractive advantages.

1. The _smart watch_ can be worn twenty-four hours a day and thus the patient will be continuously monitored (with some breaks for recharging the device).
2. On the watch itself we can implement algorithms that correlate blood oxidation with heart rate and thus make the predictions more robust against false alarms.
3. Using continuously collected data allows a much better quality of prediction than one single measure taken every day. This also adds to the robustness against false alarms.
4. Imagine for example, if a person living alone faints due to hypoxia, the _smart phone_ could be programmed to issue an emergency call to a predefined phone number, e.g. a neighbor who can look after the patient, or the patient’s physician (calling the emergency automatically, is probably not such a good idea, because of false alarms).
5. The data collected by the _smart-watch_ is usually uploaded to a cloud. Making this data available to the physician, he can survey his Corona-patients on a daily basis without the need to visit or call. This data could be enriched by the patient reporting his subjective state of health.
6. Provided that the patient and the physician agree to share the data from the cloud, we (the programmers) have a means to continuously improve our prediction algorithms on the basis of real empirical data.
7. Last not least, the _smart-watch_ will turn out to be a nice gadget used much more for leisure than for patient monitoring.

# The project 

In this project we propose to realize a system composed of two parts. One part is implemented on the _smart watch_ itself. The other part is implemented on the _smart phone_. The smart watch and the  smart phone communicate as usual trough Bluetooth Low Energy (BLE) 

## Smart Watch Part
On the _smart watch_ itself we implement the algorithms that interpret the readings from the SpO2 sensors, compare them to previous readings, do the same with heart rate readings and finally decide whether __hypoxia alarm__ should be given.

Furthermore, the _smart watch_ must have the means of __self testing__. That is, the smart watch must be able to monitor the status of its battery and the correct functioning of its SpO2 sensors.

## Smart Phone Part
The smart phone is mainly used to visualize the readings of the watch and to communicate the alarms.


