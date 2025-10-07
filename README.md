# Ex09 Event Registration Web Application
## Date:7.10.2025

## AIM:
To design, develop and deploy a web application for event registration.

## DESIGN STEPS:

### Step 1:
Create a new frame.

### Step 2:
Select any one preset size of your choice.

### Step 3:
Select the shapes you need.

### Step 4:
Import images as needed.

### Step 5:
Create pages based on your need and link them.

### Step 6:

Validate the HTML and CSS code.

### Step 6:

Publish the website in the given URL.

## DESIGN TOOL:
Figma

## CODE:
```
frame 1
import React from "react";
import screenshot202510071551561 from "./screenshot-2025-10-07-155156-1.png";

export const Iphone = (): JSX.Element => {
  return (
    <div className="bg-white w-full min-w-[393px] min-h-[852px] relative">
      <img
        className="absolute top-0 left-0 w-[393px] h-[852px] aspect-[1.97] object-cover"
        alt="Screenshot"
        src={screenshot202510071551561}
      />

      <h1 className="absolute top-[66px] left-[25px] [font-family:'Inter-Bold',Helvetica] font-bold text-[#e71759] text-[40px] tracking-[0] leading-[normal] whitespace-nowrap">
        HOLY FEST
      </h1>

      <button
        className="absolute top-[416px] left-[38px] w-[355px] h-[103px] bg-[#d9d9d9] cursor-pointer hover:bg-[#c9c9c9] transition-colors"
        aria-label="Register for Holy Fest"
      >
        <span className="absolute top-[29px] left-[49px] [font-family:'Inter-Bold',Helvetica] font-bold text-black text-5xl tracking-[0] leading-[normal]">
          REGISTER
        </span>
      </button>
    </div>
  );
};


/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./src/**/*.{html,js,ts,jsx,tsx}"],
  theme: {
    extend: {},
  },
  plugins: [],
};

@tailwind base;
@tailwind components;
@tailwind utilities;

@layer base {
  button,
  input,
  select,
  textarea {
    @apply appearance-none bg-transparent border-0 outline-none;
  }
}

@tailwind components;
@tailwind utilities;

@layer components {
  .all-\[unset\] {
    all: unset;
  }
}

:root {
  --animate-spin: spin 1s linear infinite;
}

.animate-fade-in {
  animation: fade-in 1s var(--animation-delay, 0s) ease forwards;
}

.animate-fade-up {
  animation: fade-up 1s var(--animation-delay, 0s) ease forwards;
}

.animate-marquee {
  animation: marquee var(--duration) infinite linear;
}

.animate-marquee-vertical {
  animation: marquee-vertical var(--duration) linear infinite;
}

.animate-shimmer {
  animation: shimmer 8s infinite;
}

.animate-spin {
  animation: var(--animate-spin);
}

@keyframes spin {
  to {
    transform: rotate(1turn);
  }
}

@keyframes image-glow {
  0% {
    opacity: 0;
    animation-timing-function: cubic-bezier(0.74, 0.25, 0.76, 1);
  }

  10% {
    opacity: 0.7;
    animation-timing-function: cubic-bezier(0.12, 0.01, 0.08, 0.99);
  }

  to {
    opacity: 0.4;
  }
}

@keyframes fade-in {
  0% {
    opacity: 0;
    transform: translateY(-10px);
  }

  to {
    opacity: 1;
    transform: none;
  }
}

@keyframes fade-up {
  0% {
    opacity: 0;
    transform: translateY(20px);
  }

  to {
    opacity: 1;
    transform: none;
  }
}

@keyframes shimmer {
  0%,
  90%,
  to {
    background-position: calc(-100% - var(--shimmer-width)) 0;
  }

  30%,
  60% {
    background-position: calc(100% + var(--shimmer-width)) 0;
  }
}

@keyframes marquee {
  0% {
    transform: translate(0);
  }

  to {
    transform: translateX(calc(-100% - var(--gap)));
  }
}

@keyframes marquee-vertical {
  0% {
    transform: translateY(0);
  }

  to {
    transform: translateY(calc(-100% - var(--gap)));
  }
}

frame 2
import React from "react";
import IMAGE21 from "./IMAGE-2-1.png";

export const AndroidMedium = (): JSX.Element => {
  const eventActivities = [
    {
      id: 1,
      text: "*TRADITIONAL GAMES",
      top: "156px",
      left: "22px",
      width: "382px",
      color: "#1e0303",
    },
    {
      id: 2,
      text: "*WATER BALLONS",
      top: "239px",
      left: "28px",
      width: "290px",
      color: "black",
    },
    {
      id: 3,
      text: "*COLOURFULL DANCE",
      top: "337px",
      left: "28px",
      width: "376px",
      color: "black",
    },
  ];

  return (
    <main className="bg-white w-full min-w-[417px] min-h-[858px] relative">
      <img
        className="absolute top-px left-0 w-[417px] h-[857px] aspect-[1.34] object-cover"
        alt="Holy Fest Events colorful celebration background"
        src={IMAGE21}
      />

      <header className="absolute top-[69px] left-[46px] [font-family:'Inter-Bold',Helvetica] font-bold text-[#ab1111] text-[32px] tracking-[0] leading-[normal]">
        <h1>HOLY FEST EVENTS</h1>
      </header>

      <section aria-label="Event activities">
        {eventActivities.map((activity) => (
          <div
            key={activity.id}
            className="absolute [font-family:'Inter-Bold',Helvetica] font-bold text-[32px] tracking-[0] leading-[normal] whitespace-nowrap"
            style={{
              top: activity.top,
              left: activity.left,
              width: activity.width,
              color: activity.color,
            }}
          >
            {activity.text}
          </div>
        ))}
      </section>

      <section
        aria-label="Event dates"
        className="absolute top-[517px] left-[73px] w-[331px]"
      >
        <div className="[font-family:'Inter-Bold',Helvetica] font-bold text-[#9d1818] text-[32px] tracking-[0] leading-[normal]">
          START&nbsp;&nbsp; FROM
        </div>

        <p className="absolute top-[74px] left-[-27px] [font-family:'Inter-Bold',Helvetica] font-bold text-[#1d0303] text-[32px] tracking-[0] leading-[normal]">
          <time dateTime="2024-10-06">6 OCT</time> TO{" "}
          <time dateTime="2024-10-20">20 OCT</time>
        </p>
      </section>
    </main>
  );
};
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./src/**/*.{html,js,ts,jsx,tsx}"],
  theme: {
    extend: {},
  },
  plugins: [],
};
@tailwind base;
@tailwind components;
@tailwind utilities;

@layer base {
  button,
  input,
  select,
  textarea {
    @apply appearance-none bg-transparent border-0 outline-none;
  }
}

@tailwind components;
@tailwind utilities;

@layer components {
  .all-\[unset\] {
    all: unset;
  }
}

:root {
  --animate-spin: spin 1s linear infinite;
}

.animate-fade-in {
  animation: fade-in 1s var(--animation-delay, 0s) ease forwards;
}

.animate-fade-up {
  animation: fade-up 1s var(--animation-delay, 0s) ease forwards;
}

.animate-marquee {
  animation: marquee var(--duration) infinite linear;
}

.animate-marquee-vertical {
  animation: marquee-vertical var(--duration) linear infinite;
}

.animate-shimmer {
  animation: shimmer 8s infinite;
}

.animate-spin {
  animation: var(--animate-spin);
}

@keyframes spin {
  to {
    transform: rotate(1turn);
  }
}

@keyframes image-glow {
  0% {
    opacity: 0;
    animation-timing-function: cubic-bezier(0.74, 0.25, 0.76, 1);
  }

  10% {
    opacity: 0.7;
    animation-timing-function: cubic-bezier(0.12, 0.01, 0.08, 0.99);
  }

  to {
    opacity: 0.4;
  }
}

@keyframes fade-in {
  0% {
    opacity: 0;
    transform: translateY(-10px);
  }

  to {
    opacity: 1;
    transform: none;
  }
}

@keyframes fade-up {
  0% {
    opacity: 0;
    transform: translateY(20px);
  }

  to {
    opacity: 1;
    transform: none;
  }
}

@keyframes shimmer {
  0%,
  90%,
  to {
    background-position: calc(-100% - var(--shimmer-width)) 0;
  }

  30%,
  60% {
    background-position: calc(100% + var(--shimmer-width)) 0;
  }
}

@keyframes marquee {
  0% {
    transform: translate(0);
  }

  to {
    transform: translateX(calc(-100% - var(--gap)));
  }
}

@keyframes marquee-vertical {
  0% {
    transform: translateY(0);
  }

  to {
    transform: translateY(calc(-100% - var(--gap)));
  }
}


frame 3
import React, { useState } from "react";
import images31 from "./images-3-1.png";
import textOnAPath from "./text-on-a-path.svg";

export const Iphone = (): JSX.Element => {
  const [formData, setFormData] = useState({
    name: "",
    email: "",
    gender: "",
    phone: "",
    department: "",
  });

  const handleInputChange = (
    e: React.ChangeEvent<HTMLInputElement | HTMLSelectElement>,
  ) => {
    const { name, value } = e.target;
    setFormData((prev) => ({
      ...prev,
      [name]: value,
    }));
  };

  const handleSubmit = (e: React.FormEvent) => {
    e.preventDefault();
    console.log("Form submitted:", formData);
  };

  return (
    <div className="bg-[#ab1111] overflow-hidden w-full min-w-[393px] min-h-[852px] relative">
      <img
        className="absolute top-0 left-0 w-[393px] h-[852px] aspect-[0.46] object-cover"
        alt="Background"
        src={images31}
      />

      <form onSubmit={handleSubmit} className="relative z-10">
        <div className="absolute top-[61px] left-6 w-[346px]">
          <label
            htmlFor="name"
            className="block [font-family:'Inter-Bold',Helvetica] font-bold text-black text-2xl tracking-[0] leading-[normal] mb-2"
          >
            NAME :
          </label>
          <input
            type="text"
            id="name"
            name="name"
            value={formData.name}
            onChange={handleInputChange}
            className="w-full px-3 py-2 bg-white/80 border-2 border-black rounded text-black [font-family:'Inter-Bold',Helvetica] font-bold"
            required
            aria-label="Name"
          />
        </div>

        <div className="absolute top-32 left-6 w-[346px]">
          <label
            htmlFor="email"
            className="block [font-family:'Inter-Bold',Helvetica] font-bold text-black text-2xl tracking-[0] leading-[normal] mb-2"
          >
            EMAIL ADDRESS:
          </label>
          <input
            type="email"
            id="email"
            name="email"
            value={formData.email}
            onChange={handleInputChange}
            className="w-full px-3 py-2 bg-white/80 border-2 border-black rounded text-black [font-family:'Inter-Bold',Helvetica] font-bold"
            required
            aria-label="Email Address"
          />
        </div>

        <div className="absolute top-[205px] left-6 w-[346px]">
          <label
            htmlFor="gender"
            className="block [font-family:'Inter-Bold',Helvetica] font-bold text-black text-2xl tracking-[0] leading-[normal] mb-2"
          >
            GENDER:
          </label>
          <select
            id="gender"
            name="gender"
            value={formData.gender}
            onChange={handleInputChange}
            className="w-full px-3 py-2 bg-white/80 border-2 border-black rounded text-black [font-family:'Inter-Bold',Helvetica] font-bold"
            required
            aria-label="Gender"
          >
            <option value="">Select Gender</option>
            <option value="male">Male</option>
            <option value="female">Female</option>
            <option value="other">Other</option>
            <option value="prefer-not-to-say">Prefer not to say</option>
          </select>
        </div>

        <div className="absolute top-[279px] left-6 w-[346px]">
          <label
            htmlFor="phone"
            className="block [font-family:'Inter-Bold',Helvetica] font-bold text-black text-2xl tracking-[0] leading-[normal] mb-2"
          >
            PHONE NUMBER:
          </label>
          <input
            type="tel"
            id="phone"
            name="phone"
            value={formData.phone}
            onChange={handleInputChange}
            className="w-full px-3 py-2 bg-white/80 border-2 border-black rounded text-black [font-family:'Inter-Bold',Helvetica] font-bold"
            required
            aria-label="Phone Number"
            pattern="[0-9]{10,15}"
          />
        </div>

        <div className="absolute top-[353px] left-[25px] w-[346px]">
          <label
            htmlFor="department"
            className="block [font-family:'Inter-Bold',Helvetica] font-bold text-black text-2xl tracking-[0] leading-[normal] mb-2"
          >
            DEPARTMENT:
          </label>
          <input
            type="text"
            id="department"
            name="department"
            value={formData.department}
            onChange={handleInputChange}
            className="w-full px-3 py-2 bg-white/80 border-2 border-black rounded text-black [font-family:'Inter-Bold',Helvetica] font-bold"
            required
            aria-label="Department"
          />
        </div>

        <img
          className="absolute top-[458px] left-[-933px] w-[393px] h-[70px]"
          alt="Decorative text on a path"
          src={textOnAPath}
          aria-hidden="true"
        />

        <div className="absolute top-[649px] left-0 w-[370px] px-6">
          <h1 className="[font-family:'Inter-Bold',Helvetica] font-bold text-black text-[32px] tracking-[0] leading-[normal] mb-6">
            FILL THE REGISTER FORM
          </h1>
          <button
            type="submit"
            className="w-full px-6 py-4 bg-black text-white [font-family:'Inter-Bold',Helvetica] font-bold text-xl rounded hover:bg-gray-800 transition-colors focus:outline-none focus:ring-4 focus:ring-black/50"
            aria-label="Submit registration form"
          >
            SUBMIT
          </button>
        </div>
      </form>
    </div>
  );
};
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./src/**/*.{html,js,ts,jsx,tsx}"],
  theme: {
    extend: {},
  },
  plugins: [],
};
@tailwind base;
@tailwind components;
@tailwind utilities;

@layer base {
  button,
  input,
  select,
  textarea {
    @apply appearance-none bg-transparent border-0 outline-none;
  }
}

@tailwind components;
@tailwind utilities;

@layer components {
  .all-\[unset\] {
    all: unset;
  }
}

:root {
  --animate-spin: spin 1s linear infinite;
}

.animate-fade-in {
  animation: fade-in 1s var(--animation-delay, 0s) ease forwards;
}

.animate-fade-up {
  animation: fade-up 1s var(--animation-delay, 0s) ease forwards;
}

.animate-marquee {
  animation: marquee var(--duration) infinite linear;
}

.animate-marquee-vertical {
  animation: marquee-vertical var(--duration) linear infinite;
}

.animate-shimmer {
  animation: shimmer 8s infinite;
}

.animate-spin {
  animation: var(--animate-spin);
}

@keyframes spin {
  to {
    transform: rotate(1turn);
  }
}

@keyframes image-glow {
  0% {
    opacity: 0;
    animation-timing-function: cubic-bezier(0.74, 0.25, 0.76, 1);
  }

  10% {
    opacity: 0.7;
    animation-timing-function: cubic-bezier(0.12, 0.01, 0.08, 0.99);
  }

  to {
    opacity: 0.4;
  }
}

@keyframes fade-in {
  0% {
    opacity: 0;
    transform: translateY(-10px);
  }

  to {
    opacity: 1;
    transform: none;
  }
}

@keyframes fade-up {
  0% {
    opacity: 0;
    transform: translateY(20px);
  }

  to {
    opacity: 1;
    transform: none;
  }
}

@keyframes shimmer {
  0%,
  90%,
  to {
    background-position: calc(-100% - var(--shimmer-width)) 0;
  }

  30%,
  60% {
    background-position: calc(100% + var(--shimmer-width)) 0;
  }
}

@keyframes marquee {
  0% {
    transform: translate(0);
  }

  to {
    transform: translateX(calc(-100% - var(--gap)));
  }
}

@keyframes marquee-vertical {
  0% {
    transform: translateY(0);
  }

  to {
    transform: translateY(calc(-100% - var(--gap)));
  }
}
frame 4
import React from "react";
import images11 from "./images-1-1.png";

export const Iphone = (): JSX.Element => {
  const textLines = [
    { text: "THANK YOU", top: "82px", width: "409px", color: "text-white" },
    { text: "FOR", top: "208px", width: "150px", color: "text-white" },
    { text: "JOINING", top: "333px", width: "283px", color: "text-black" },
    { text: "WITH US...", top: "473px", width: "371px", color: "text-black" },
  ];

  return (
    <main className="bg-white overflow-hidden w-full min-w-[407px] min-h-[852px] relative">
      <img
        className="absolute top-0 left-0 w-[407px] h-[852px] aspect-[1.5] object-cover"
        alt="Colorful gradient background"
        src={images11}
      />

      {textLines.map((line, index) => (
        <div
          key={index}
          className={`absolute left-0 [font-family:'Inter-Bold',Helvetica] font-bold ${line.color} text-[64px] tracking-[0] leading-[normal] ${line.text === "WITH US..." ? "whitespace-nowrap" : ""}`}
          style={{ top: line.top, width: line.width }}
        >
          {line.text}
        </div>
      ))}
    </main>
  );
};
/** @type{import('tailwindcss').config} */
module.exports ={
    content:["./src/**/*.{html,js,ts,jsx,tsx}"],
    theme: {
        extend: {}
    },
    plugins: [],
};
@tailwind base;
@tailwind components;
@tailwind utilities;

@layer base {
    button,
    input,
    select,
    textarea {
        @apply appearance-none bg-transparent border-0 outline-none;
    }    
}
@tailwind components;
@tailwind utilities;

@layer components {
    .all-[unset\]{
        all: unset;
    }
}
:root {
    --animate-spin: spin 1s linear infinite;
}
.animate-fade-in {
    animation: fade-in 1s var(--animation-delay,0s) ease forwards;
}
.animate-fade-up {
    animation: fade-up 1s var(--animation-delay,0s) ease farwards;
}
.animate-marquee {
    animation: marquee-vertical var(--duration)infinite linear;
}
.animate-marquee-vertical {
    animation: marquee-vertical var(--duration)linear infinite;
}
.animate-shimmer {
    animation;shimmer 8s infinite;
}
.animate-spin {
    animation: var9(--animate-spin);
}
@keyframes spin {
    to {
        transform: rotate(1turn);
    }
}
@keyframes image-glow {
    0% {
        opacity:0;
        animation-timing-function:cubic-bezier(0.74,0.25,0.76,1);
    }
    10% {
        opacity: 0.7;
        animation-timing-function: cubic-bezier(0.12,0.01,0.08,0.99);
    }
    to {      
            opacity: 0.4;
        }
    }
@keyframes fade-in {
    0% {
        opacity: 0;
        transform: translateY(-10px);
    }
    to {
        opacity: 1;
        transform: none;
    }
}
@keyframes fade-up {
    0% {
        opacity: 0;
        transform: translateY(20px);
    }
    to {
        opacity: 1;
        transform: none;
    }
}
@keyframes shimmer {
    0%
    90%
    to {
        background-position: calc(-100% -var(--shimmer-width))0;
    }
    30%
    60% {
        background-position: calc(100% + var (--shimmer-width))0;
    }
}
@keyframes marquee {
    0% {
        transform: translateX(calc(-100% -var(--gap)));
    }
}
@keyframes margquee-vertical {
    0% {
        transform: translateY(0);
    }
to {
    transform: translate(calc(-100% -var(--gap)))
}
}

```


    


## OUTPUT:
![alt text](<Screenshot 2025-10-07 174719.png>)

## RESULT:
The program to design, develop and deploy a web application for event registration is completed successfully.
