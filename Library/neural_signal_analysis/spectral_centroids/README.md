<div style="font-size: 13px; font-family: 'Times New Roman', Times, serif; background-color: #181818; color: #D0D0D0; padding: 20px; border-radius: 8px; margin: 10px; display: flex; flex-wrap: nowrap; justify-content: space-between;">
    <!-- Column 1 -->
    <div style="flex: 1; margin-right: 10px;">
        <h2>Introduction</h2>
        <p>This code aims to assess the spectral characteristics of EEG data by calculating the spectral centroid for each channel. The spectral centroid is a feature that is often used to describe a frequency spectrum and serves as a sort of 'center of mass' for the spectrum. Understanding this feature can give us insights into the characteristics of the EEG signal in different brain regions.</p>
         <p>The Fourier Transform allows us to convert our time-domain signal into its frequency domain representation. Mathematically, it is expressed as:</p>
        \[
        F(f) = \int_{-\infty}^{\infty} x(t) e^{-2\pi ift} dt
        \]
        <p>This transformation is implemented in the code using the <code>scipy.fft.fft</code> function, which provides us with \( F(f) \), the Fourier Transform of the signal.</p>
    </div>
    <!-- Column 2 -->
    <div style="flex: 1; margin-left: 10px;">
               <p>Once in the frequency domain, the spectral centroid \( C \) for a signal is calculated as:</p>
        \[
        C = \frac{\sum_{n=0}^{N-1} f(n) \times |X(f(n))|}{\sum_{n=0}^{N-1} |X(f(n))|}
        \]
        <p>Here, \( f(n) \) are the frequencies associated with the Fourier Transform values. These frequencies are generated by the function <code>scipy.fft.fftfreq</code> in the code. \( |X(f(n))| \) represents the magnitude of the Fourier Transform at those frequencies, calculated as the absolute value of the complex Fourier coefficients.</p>
        <p>The spectral centroid provides a weighted average of the frequency components, effectively giving us a single scalar that characterizes the distribution of energy across frequencies. In the code, this is stored in the <code>spectral_centroids</code> dictionary, with one entry per EEG channel.</p>
    </div>
</div>