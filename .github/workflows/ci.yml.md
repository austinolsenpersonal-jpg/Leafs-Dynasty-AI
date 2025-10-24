**name: CI**



**on:**

  **push:**

    **branches: \[ main, master ]**

  **pull\_request:**

    **branches: \[ main, master ]**



**jobs:**

  **sanity:**

    **name: Sanity Check**

    **runs-on: ubuntu-latest**

    **steps:**

      **- name: Checkout**

        **uses: actions/checkout@v4**

      **- name: CI alive**

        **run: echo "Leafs Dynasty AI CI is on ✅"**



