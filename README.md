
:root {
  --primary-color: #000000;
  --secondary-color: #5682B1;
  --background-color: #FFE8DB;
  --container-max: 1200px;
  --gap: 2rem;
}

*, *::before, *::after {
  box-sizing: border-box;
}

html, body {
  height: 100%;
  margin: 0;
}

body {
  background-color: var(--background-color);
  color: var(--primary-color);
  display: flex;
  align-items: center;
  justify-content: center;
}

section {
  width: min(100%, var(--container-max));
  padding: 4rem var(--gap);
}

section > p {
  font-size: clamp(1.2rem, 2.5vw + 0.5rem, 2.5rem);
  text-align: center;
  padding-block-start: 3rem;
  font-family: system-ui, -apple-system, "Segoe UI", Roboto, "Open Sans", sans-serif;
}

section > .container > h1 {
  font-size: clamp(1rem, 1.5vw + 0.8rem, 1.6rem);
  text-align: center;
  font-family: Poppins, sans-serif;
  margin: 0;
}

#tick {
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 1rem var(--gap);
}

#tick > .time {
  font-family: Poppins, sans-serif;
  font-size: clamp(1.2rem, 2vw, 2rem);
  border: 0.5rem solid var(--primary-color);
  border-radius: 999px;
  width: 13rem;
  height: 2.5rem;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  color: var(--primary-color);
}

.tap {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: var(--gap);
  padding: 2rem var(--gap);
}

.tap > button {
  font-size: 1rem;
  padding: 0.75em 1.75em;
  background-color: var(--primary-color);
  color: var(--background-color);
  border: none;
  border-radius: 999px;
  box-shadow: 3px 2px 3px rgba(0, 0, 0, 0.2);
  cursor: pointer;
  transition: transform 0.2s ease;
}

.tap > button:active {
  transform: translateY(1px) scale(0.98);
}


@media (max-width: 1024px) {
  section { padding: 3rem var(--gap); }
  #tick { padding-inline: var(--gap); }
}

@media (max-width: 600px) {
  #tick { padding-inline: var(--gap); }
  #tick > .time { width: 11rem; }
  .tap { padding: 1rem var(--gap); }
}
