# Tiuri Health

> Starter cloned from [nextjs/saas-starter](https://github.com/nextjs/saas-starter)


## Links

- [Marketing website](https://www.tiurihealth.com/)
- [Product definition](https://docs.google.com/document/d/1e2b9vgsu-KEjWirE1poZquM_4GoeuL3ut-wqVJDin94/edit?tab=t.0)
- [Brand book](https://docs.google.com/document/d/1iY97Bggw13DtzcDU7i6PQQfUdO-l1_R1nbcSII99nEE/edit?tab=t.0#heading=h.7fmr1v24kmly)

- [App preview](https://tiurihealth-app.vercel.app/)
- [Github Repo](https://github.com/tiurihealth/tiurihealth)
- [Neon Database](https://console.neon.tech/app/projects/gentle-star-89097860?branchId=br-bold-truth-abcjd8ir&database=neondb)
- [Stripe Dashboard](https://dashboard.stripe.com/test/dashboard)

### Similar projects

- [Nozomi Health](https://studio.nozomihealth.com/)
- [Neko Health](https://www.nekohealth.com/se/en)

### 3D Visualiazionts

- [Medical Graphics 3D body visualizations](https://www.medicalgraphics.de/en/project/anatomical-3d-models-in-web-browser/)
- [BioCloud 3D Anatomy](https://www.intervoke.com/biocloud3d-anatomy)
- [WebXR](https://immersiveweb.dev/#react-xr)

### Wearables' APIs

- Products
  - [Spike - 360° Health Data API. Connect to 500+ wearables, IoT sensors, EMRs and lab systems](https://www.spikeapi.com/)
  - [Rook - SOLVE WEARABLE INTEGRATION PROBLEMS WITH ROOK’S API](https://www.tryrook.io/wearable-api/integrations)
  - [Terra - The Health API for Wearable and Sensor Data](https://tryterra.co/)

- Articles
  - [10 Best Fitness API Providers](https://www.sportfitnessapps.com/blog/10-best-fitness-api-providers)


### Data

- List of trackable indicators from [tryterra.co/blog](https://tryterra.co/blog/comprehensive-list-of-all-the-wearable-data-that-are-available-through-apis-2bcd35a7307f):
  - Heart rate
  - Heart rate variability
  - Blood oxygen measurement (Pulse OX)
  - Respiration rate
  - Sleep
  - Body temperature
  - GPS
  - Accelerometer
  - Glucose

## Notes

### Design

- We start with wireframes and build the functionalities quite naked, then we dress them based on the branding agency guidelines and decisions we make along the way.
- We can start thinking about fluent flows which bring you from the 3d visualization to the metrics/scores view showing the areas of improvements, I can think about timlines dotted charts or donuts/rings charts, something that gives a perspective on future possible improvements and stimulates patients to work on themselves and get a next appointment.
- We could use Stitch to help with design (AI assisted)

Screens to sketch:
- basic auth (not so crucial)
- booking appointment
- dashboard with data visualization, maybe three views/perspectives:
  - **user**: from the app or website
  - **doctor**: from a ipad or directly on the studio's monitor
  - **appointment**:

- think about 3d visualization of the body, which kind of texture (Neko ussed blue dots) would be cool to apply to get a fancy stylised representation of it. Otherwise the branding agency can propose that.

### Architecture

- Think about wether to start with an app or with a website. See compatibility with looking glass which can uses ipad to control the view as in [this video](https://youtu.be/b6Qb-w9DT60). We can either start with the application with react native, and parallely build a simple website which hosts parts of the website like the booking module which can be embedded in either the app or the marketing website. The best would probably be to build everything in react with the least dependencies on either NextJS (website) or React Native (app) so that we can share the most code in either case. Especially the 3d view let's try to use the most standrd WebGL and WebXR technologies.
  - Consider that on the appointment the screen used (if we don't go for the looking glass) will have a high resolution
  - Consider we want an immersive experience during the appointment so no standard Android or iOS default UIs but a full screen view

- Booking appointment module:
  - see Serghei scheduler proposal or consider some simple SaaS or even Google Calendar API's integration

### Next steps

On Tuesday 9th September or for the first week a clear idea of the architecture of the project, and some wireframes which put on paper the screens, the UX flows, etc. By the end of the or sooner let's try to have a timeline with steps, the idea is to go live by the end of year, see if it's doable.
