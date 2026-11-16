# Отложенная стабилизация в квантовом измерении / Delayed Stabilization in Quantum Measurement

[![Interactive Demo](https://img.shields.io/badge/Interactive_Demo-Open_Web_App-blue?style=for-the-badge&logo=googlechrome&logoColor=white)](https://vasiliypavlov.github.io/predelayed-stabilization/)
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.24252176.svg)](https://doi.org/10.5281/zenodo.24252176)

**Открытая исследовательская гипотеза и предложение эксперимента**

В этом репозитории представлена феноменологическая гипотеза: **результаты квантового измерения могут фиксироваться не мгновенно, а возникать в ходе кратковременного процесса стабилизации с характерным временем $\tau_{\mathrm{stab}}$.**

Основная идея — исследовать *временну́ю структуру* перехода от суперпозиции к определённому исходу на сверхкоротких масштабах ($t \lesssim \tau_{\mathrm{stab}}$). В асимптотическом пределе завершённого измерения ($t \gg \tau_{\mathrm{stab}}$) модель полностью воспроизводит стандартную борновскую статистику.

**An Open Research Hypothesis and Experimental Proposal**

This repository presents a phenomenological hypothesis: **quantum measurement outcomes may not be fixed instantaneously but could emerge through a brief, finite-time “stabilization” process with a characteristic timescale $\tau_{\mathrm{stab}}$.**

The core idea is to explore the *temporal structure* between superposition and a definite outcome on ultrashort timescales ($t \lesssim \tau_{\mathrm{stab}}$). In the asymptotic limit of a completed measurement ($t \gg \tau_{\mathrm{stab}}$), the model reproduces standard Born statistics exactly.

---

## 🖥️ Интерактивный симулятор / Interactive Testbed Simulator

Вы можете протестировать математическую модель в реальном времени прямо в браузере без установки дополнительного ПО:

* 🚀 **[Запустить интерактивный стенд МЦИ (GitHub Pages)](https://vasiliypavlov.github.io/predelayed-stabilization/)**
* 📄 **[Исходный код симулятора (`index.html`)](index.html)** — автономное однофайловое приложение (HTML5 Canvas + Vanilla JS), позволяющее варьировать $\tau_{\mathrm{stab}}$, базовое время контура $T_0$ (платформы Si<sub>3</sub>N<sub>4</sub>, SOI и 4f-стенд), фазу $\varphi$, видность $V$, сдвиги указателей $\delta x/\sigma$, инверсию знака и дробовой шум на статистике до $10^{10}$ фотонов.

You can explore the mathematical model in real time directly in your browser with zero server-side dependencies:

* 🚀 **[Launch Interactive MZI Simulator (GitHub Pages)](https://vasiliypavlov.github.io/predelayed-stabilization/)**
* 📄 **[Simulator Source Code (`index.html`)](index.html)** — standalone single-file application (HTML5 Canvas + Vanilla JS) supporting parameter sweeps over $\tau_{\mathrm{stab}}$, baseline loop transit time $T_0$ (Si<sub>3</sub>N<sub>4</sub>, SOI, and 4f free-space platforms), phase $\varphi$, visibility $V$, pointer displacements $\delta x/\sigma$, single-axis sign inversion, and Monte Carlo shot-noise simulation up to $10^{10}$ photons.

---

## 🎯 Суть гипотезы / The Core Idea

В стандартных интерпретациях переход к определённому исходу часто трактуется как мгновенный («коллапс») или описывается через декогеренцию, без рассмотрения динамики *того, как* выбирается один результат.

**Гипотеза об отложенной стабилизации** предлагает иной взгляд:  
До момента финальной детекции могут временно сосуществовать фазово-согласованные ветви эволюции. Определённое событие регистрации детектора соответствует не мгновенному скачку, а динамической стабилизации одного такого ансамбля — процессу, занимающему конечное время $\tau_{\mathrm{stab}}$ и описываемому локальным CPTP-каналом с сохранением принципа запрета сверхсветовой передачи сигнала (`no-signaling`).

In standard interpretations, the transition to a definite outcome is often treated as instantaneous (“collapse”) or described via decoherence without addressing the dynamics of *how* one outcome is selected.

The **Delayed Stabilization Hypothesis** suggests a different perspective:  
Prior to final detection, phase-coherent evolutionary branches may temporarily coexist. A definite detector event corresponds not to an instantaneous jump, but to the **dynamic stabilization** of one consistent ensemble — a process occupying a finite timescale $\tau_{\mathrm{stab}}$ and formulated via a local CPTP channel strictly preserving the `no-signaling` principle.

---

## 📄 Файлы / Files

### 🇷🇺 Русскоязычные материалы

* **[Основной препринт](paper/predelayed_stabilization_core_preprint_ru.md)** — научная формулировка гипотезы, CPTP-модель, расчёт статистики фотонов и описание эксперимента.
* **[Интерактивный симулятор](index.html)** — веб-приложение для моделирования режимов задержки (Mode I и Mode II Null Control).

### 🇺🇸 English materials

* **[Core Preprint](paper/predelayed_stabilization_core_preprint_en.md)** — scientific formulation of the hypothesis, CPTP channel model, photon budget analysis, and experimental proposal.
* **[Interactive Simulator](index.html)** — standalone browser-based testbed for simulating delay regimes (Mode I and Mode II Null Control).

---

## 🔬 Предлагаемый экспериментальный тест / Proposed Experimental Test

Гипотеза приводит к фальсифицируемому предсказанию: **короткоживущие избыточные корреляции второго порядка $\Delta C(\Delta t) = C(\Delta t) - C_{\mathrm{QM}}(\varphi, V)$ между ортогональными пространственными указателями $(x, y)$ одиночного фотона до рекомбинации на выходном светоделителе BS<sub>2</sub>.**

Протокол эксперимента описан в Основном препринте и включает две архитектуры:

1. **Наносекундный диапазон ($\tau_{\mathrm{stab}} \gtrsim 2$ нс):** сбалансированный интерферометр Маха–Цендера в свободном пространстве с 4f-ретранслирующими телескопическими линиями задержки, наклонными стеклянными пластинами слабого сдвига $(\delta x, \delta y)$ и координатно-чувствительной 2D-SPAD-матрицей.
2. **Пикосекундный диапазон ($\tau_{\mathrm{stab}} \sim 1\text{—}100$ пс):** многомодовый интегрально-фотонный интерферометр на чипе (Si<sub>3</sub>N<sub>4</sub> / SOI) с использованием ортогональных волноводных мод TE<sub>10</sub> и TE<sub>01</sub>.

The hypothesis leads to a falsifiable prediction: **transient second-order excess correlations $\Delta C(\Delta t) = C(\Delta t) - C_{\mathrm{QM}}(\varphi, V)$ between orthogonal transverse spatial pointers $(x, y)$ of a single photon prior to recombination at the output beam splitter BS<sub>2</sub>.**

The experimental protocol is detailed in the Core Preprint across two platforms:

1. **Nanosecond regime ($\tau_{\mathrm{stab}} \gtrsim 2$ ns):** a balanced free-space Mach–Zehnder interferometer featuring 4f-relayed optical delay lines, tilted plane-parallel glass plates for polarization-independent shifts $(\delta x, \delta y)$, and a position-sensitive 2D SPAD array.
2. **Picosecond regime ($\tau_{\mathrm{stab}} \sim 1\text{—}100$ ps):** a multimode integrated-photonic chip MZI (Si<sub>3</sub>N<sub>4</sub> / SOI) utilizing orthogonal waveguide modes TE<sub>10</sub> and TE<sub>01</sub>.

---

## 🔑 Ключевые слова / Keywords

**Ключевые слова:** квантовое измерение, отложенная стабилизация, слабые измерения, интерферометр Маха–Цендера, квантовые траектории, декогеренция, спонтанный коллапс, немарковская динамика.

**Keywords:** quantum measurement, delayed stabilization, weak measurements, Mach–Zehnder interferometer, quantum trajectories, decoherence, objective collapse, non-Markovian dynamics.

---

## ⚖️ Лицензия / License

**Author:** Vasiliy Pavlov

* **Research papers and documentation (`paper/`, PDF):** licensed under [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0)](https://creativecommons.org/licenses/by-nc-sa/4.0/).
* **Interactive simulator source code (`index.html`):** licensed under the [MIT License](https://opensource.org/license/mit).
