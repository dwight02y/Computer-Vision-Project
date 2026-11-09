# bc_test image sources

The 90 test images (`bc_test/images/`) are **not redistributed** in this repository: most are from news and web pages and we do not have the right to share them. `bc_test/labels/` (YOLO .txt, class 0 = fire, 1 = smoke; empty file = negative image) and `config_bc.yaml` are included. To rebuild the test set, download each image from the page below and save it as `bc_test/images/<file>.<ext>` (the file name must match the label name).

Photos we took ourselves (11) are listed as `own photo`. Source pages (79) are in the table; several are negative images (kettles, light bulbs, clouds, fog, steam, factory smoke) used to test false alarms.

| File | Type | Source |
|---|---|---|
| dy_img01 | web/news | https://thenarwhal.ca/bc-wildfires-data/ |
| dy_img02 | web/news | https://cbc.ca/news/canada/british-columbia/need-to-know-bc-wildfires-aug-12-9.7304156 |
| dy_img03 | web/news | https://ici.radio-canada.ca/rci/en/news/2004910/full-extent-of-b-c-wildfire-damage-still-not-known-as-province-consumed-by-worsening-air-quality |
| dy_img04 | web/news | https://timescolonist.com/local-news/bc-wildfire-season-expect-an-early-intense-battle-as-drought-lingers-8368985 |
| dy_img05 | web/news | https://vancouver.citynews.ca/2023/06/05/bc-wildfire-season-forecast-2/ |
| dy_img06 | web/news | https://richmond-news.com/opinion/column-hot-dry-weather-hitting-bc-hard-all-of-us-should-pay-attention-7310968 |
| dy_img07 | web/news | https://cbc.ca/news/canada/british-columbia/increased-fall-wildfire-risk-1.7321883 |
| dy_img08 | web/news | https://kelownadailycourier.ca/news/national_news/article_114a62da-7bd6-5f34-a37d-1133836c9f59.html |
| dy_img09 | web/news | https://www2.gov.bc.ca/gov/content/safety/wildfire-status/wildfire-response/about-wildfire |
| dy_img10 | web/news | https://cbc.ca/news/canada/british-columbia/bc-wildfires-lightning-9.7275420 |
| dy_img11 | web/news | https://cbc.ca/news/canada/british-columbia/air-freshens-in-parts-of-b-c-while-other-regions-still-face-air-quality-fire-risks-1.4798067 |
| dy_img12 | web/news | https://radionl.com/2023/08/17/bc-wildfire-service-warns-of-extreme-fire-behaviour-due-to-heat-wave-and-dry-winds/ |
| dy_img13 | web/news | https://peacearchnews.com/2026/06/17/wildfire-west-of-princeton-grows-to-57-hectares-evacuation-alert-issued/ |
| dy_img14 | web/news | https://timescolonist.com/local-news/bc-wildfire-evacuees-told-to-brace-for-devastation-as-rcmp-launch-criminal-probe-12650568 |
| dy_img15 | web/news | https://kelownanow.com/watercooler/news/news/Provincial/Every_second_counts_BC_Wildfire_Service_to_use_new_technology_to_track_fire_growth_behaviour/ |
| dy_img16 | web/news | https://share.google/HjAzNfIlZllR5oqzP |
| dy_img17 | web/news | https://pasadenastarnews.com/2020/09/09/watch-bobcat-fire-progression-in-time-lapse-videos-from-mt-wilson/ |
| dy_img18 | web/news | https://dongascience.com/en/news/68208 |
| dy_img19 | web/news | https://petapixel.com/2021/07/28/wildfire-camera-captures-itself-getting-engulfed-by-flames/ |
| dy_img20 | web/news | https://sfchronicle.com/california-wildfires/article/See-dramatic-time-lapse-images-of-wildfire-15496690.php |
| dy_img21 | web/news | https://news.sky.com/video/cctv-camera-engulfed-in-flames-as-california-battles-wildfires-13212836 |
| dy_img22 | web/news | https://freep.com/story/news/local/michigan/2026/07/16/canada-wildfire-smoke-clouds-skies-in-mackinac-bridge-live-cam/90926333007/ |
| dy_img23 | web/news | https://dailyhive.com/vancouver/metro-vancouver-wildfire-smoke-air-quality-temperatures |
| dy_img24 | web/news | https://abcnews.com/US/canadian-wildfire-smoke-descends-us-spreading-great-lakes/story?id=134774391 |
| dy_img25 | web/news | https://adorama.com/alc/tips-for-fog-photography/ |
| dy_img26 | web/news | https://treehugger.com/types-fog-you-didnt-know-had-names-4869285 |
| dy_img27 | web/news | https://magnific.com/free-photo/dramatic-misty-mountain-landscape-with-pine-forest_427022716.htm |
| dy_img28 | web/news | https://uk.pinterest.com/pin/729723945859808627/ |
| dy_img29 | web/news | https://sciencing.com/cure-smoke-pollution-factories-23979/ |
| dy_img30 | web/news | https://scmp.com/news/china/article/1130848/factory-smoke-clouds-china-pollution-pledges |
| img1 | web | https://stockcake.com/i/illuminated-light-bulb_157140_21664 |
| img2 | web | https://www.ebay.co.uk/itm/163746580945 |
| img3 | web | https://www.sciencing.com/info-8068108-smoke-stacks/ |
| img4 | web | https://www.reddit.com/r/pittsburgh/comments/1jgo9un/the_tallest_smokestack_in_the_us1217_feet_tallat/ |
| img5 | web | https://www.pexels.com/search/burning%20paper/ |
| img6 | web | https://www.pexels.com/search/burning%20paper/ |
| img7 | web | https://www.pexels.com/search/burning%20paper/ |
| img8 | web | https://abc30.com/post/planet-vegan-fresno-food-truck-fire-explosion/11999243/ |
| img9 | web | https://deerassociation.com/food-plots-feed-or-fire-the-real-costs-per-pound-of-deer-forage/ |
| img10 | web | https://japantoday.com/category/features/health/smoke-from-la-fires-exposed-millions-of-people-to-high-levels-of-toxic-heavy-metals-study-says |
| img11 | web | https://www.japantimes.co.jp/news/2026/10/30/asia-pacific/science-health/indonesia-wildfire-toll/ |
| img12 | web | https://education.nationalgeographic.org/resource/megafire/ |
| img13 | web | https://en.wikipedia.org/wiki/Steam |
| img14 | web | https://www.usgs.gov/media/images/vapor-pressure-and-water |
| img15 | web | https://ehs.lbl.gov/service/cryogenic-liquid-safety/dry-ice-safety/ |
| img16 | web | https://westairgases.com/blog/dry-ice-blasting-uses/ |
| img17 | web | https://www.scienceabc.com/eyeopeners/dry-ice-can-make-home |
| img18 | web | https://www.polaricecorp.com/dry-ice |
| img19 | web | https://www.everypixel.com/image-7884211172519047505 |
| img20 | web | https://www.piquenewsmagazine.com/must-reads/unintential-fire-deaths-5485912 |
| img21 | web | https://www.bancroftfire.ca/main-causes-of-fire/ |
| img22 | web | https://www.icicilombard.com/blog/home-insurance/hoi/fire-accidents-don-t-let-your-home-be-a-casualty |
| img23 | web | https://www.ctvnews.ca/ottawa/article/ottawa-firefighters-douse-dunrobin-home-engulfed-in-flames-overnight/ |
| img24 | web | https://sfstandard.com/2026/08/11/big-sur-timber-wildfire-forces-evacuations-along-coast/ |
| img25 | web | https://eos.org/articles/fast-severe-wildfires-can-change-how-forests-grow-back |
| img26 | web | https://www.britannica.com/science/forest-fire |
| img27 | web | https://www.workbc.ca/career-profiles/firefighters |
| img28 | web | https://www.opb.org/article/2026/07/09/oregon-wildland-firefighters-prepare-for-potentially-busy-fire-season/ |
| img29 | web | https://www.tiny.ca/services/fire-and-emergency-services/firefighter-recruitment |
| img30 | web | https://www.workwild.ca/careers/wildland-firefighter |
| img1-kettle | web | https://naturehike.ca/en/products/kettle-camping-0-8l-feast-t3 |
| img2-kettle | web | https://www.amazon.ca/Oggi-Whistling-Tea-Pot-Blue/dp/B092PGM8FJ |
| img3-wildfire | web | https://www.aptnnews.ca/national-news/northern-ontario-fires-prompt-large-scale-evacuations-destroy-homes-in-first-nation/ |
| img4-lightbulb | web | https://www.familyhandyman.com/list/light-bulb-guide-how-to-choose-led-bulbs/ |
| img5-lightbulbs | web | https://www.superbrightleds.com/blog/all-about-led-filament-bulbs.html |
| img6-leds | web | https://shop.sheridannurseries.com/products/solar-led-paper-lantern-stringlights-14-5ft |
| img7-clouds | web | https://en.wikipedia.org/wiki/Noctilucent_cloud |
| img8-clouds | web | https://www.pacificflying.com/what-are-different-types-of-clouds/ |
| img9-clouds | web | https://www.theguardian.com/australia-news/2026/sep/15/iridescent-rainbow-clouds-phenomenon-seen-victoria-australia |
| img10-clouds | web | https://www.severe-weather.eu/learnweather/severe-weather-theory/mammatus-clouds-mk/ |
| color-night-vision-camera-image | web | https://reolink.com/blog/color-night-vision-security-cameras-buying-guide/ |
| img11-wildfire | web | https://www.dw.com/en/norway-huge-fire-destroys-100-homes-sparks-evacuations/a-78019089 |
| img12-wildfire | web | https://ici.radio-canada.ca/rci/en/news/2131362/wildfires-rage-through-l-a-forcing-thousands-to-flee-as-homes-businesses-burn |
| img13-wildfire | web | https://guelph.ctvnews.ca/atlantic/nova-scotia/article/10-wildfires-burning-two-out-of-control-in-new-brunswick/ |
| img14-wildfire | web | https://www.timminstoday.com/local-news/forest-fire-update-683469 |
| img15-greasefire | web | https://internationalfireandsafetyjournal.com/how-to-put-out-a-grease-fire/ |
| img16-carfire | web | https://www.ckom.com/2026/08/28/video-of-arson-at-toronto-mps-home-shows-suspect-dousing-vehicles-before-fires-set/ |
| img17-fire | web | https://www.ontrack.com/en-us/case-studies/surveillance-footage-recovery-from-fire-damaged-camera |
| img18-fire | web | https://www.abc.net.au/news/2016-05-07/fort-mcmurray-fires-home-security-camera-captures-inferno/7392972 |
| PXL_20230923_013507272.ACTION_PAN-01.COVER | own photo | - |
| PXL_20240107_012954283 | own photo | - |
| PXL_20240701_034858922 | own photo | - |
| PXL_20241230_004816596 | own photo | - |
| PXL_20241230_022748341 | own photo | - |
| PXL_20241230_030353560 | own photo | - |
| PXL_20260426_005030886 | own photo | - |
| PXL_20260907_020647001 | own photo | - |
| PXL_20261027_022135142 | own photo | - |
| PXL_20261027_064957070 | own photo | - |
| 20191227_163840 | own photo | - |
