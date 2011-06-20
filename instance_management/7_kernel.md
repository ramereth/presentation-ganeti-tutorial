!SLIDE redcode medtable

# Xen-PVM Kernel

<table class="rdata">
    <tr class="odd">
        <td><code><b>kernel_path</b></code></td>
        <td>valid file on node(s)</td>
    </tr>
    <tr class="even">
        <td><code><b>initrd_path</b></code></td>
        <td>valid initrd file</td>
    </tr>
    <tr class="odd">
        <td><code><b>kernel_args</b></code></td>
        <td>e.g. <code>ro quiet</code></td>
    </tr>
    <tr class="even">
        <td><code><b>root_path</b></code></td>
        <td>e.g. <code>/dev/vda2</code></td>
    </tr>
    <tr class="odd">
        <td><code><b>bootloader_path / bootloader_args</b></code></td>
        <td>to empty</td>
    </tr>
</table>

!SLIDE redcode medtable

# Xen + pvgrub

<table class="rdata">
    <tr class="odd">
        <td><code><b>kernel_path</b></code></td>
        <td>points to <code>pvgrub</code></td>
    </tr>
    <tr class="even">
        <td><code><b>kernel_args</b></code></td>
        <td>path of grub config file</td>
    </tr>
    <tr class="odd">
        <td><code><b>root_path</b></code></td>
        <td><b>must</b> be empty</td>
    </tr>
    <tr class="even">
        <td><code><b>bootloader_path / bootloader_args</b></code></td>
        <td>to empty</td>
    </tr>
</table>

!SLIDE redcode medtable

# KVM Kernel

<table class="rdata">
    <tr class="odd">
        <td><code><b>kernel_path</b></code></td>
        <td>Valid file on node(s) <i>OR</i> empty to use from instance disk.</td>
    </tr>
    <tr class="even">
        <td><code><b>initrd_path</b></code></td>
        <td>valid initrd file</td>
    </tr>
    <tr class="odd">
        <td><code><b>kernel_args</b></code></td>
        <td>e.g. <code>ro quiet</code></td>
    </tr>
    <tr class="even">
        <td><code><b>root_path</b></code></td>
        <td>e.g. <code>/dev/vda2</code></td>
    </tr>
</table>
