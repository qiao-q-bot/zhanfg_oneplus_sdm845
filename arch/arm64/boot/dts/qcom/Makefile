# SPDX-License-Identifier: GPL-2.0
# dtb-$(CONFIG_ARCH_QCOM)	+= apq8016-sbc.dtb
# dtb-$(CONFIG_ARCH_QCOM)	+= apq8096-db820c.dtb
# dtb-$(CONFIG_ARCH_QCOM)	+= ipq8074-hk01.dtb
# dtb-$(CONFIG_ARCH_QCOM)	+= msm8916-mtp.dtb
# dtb-$(CONFIG_ARCH_QCOM)	+= msm8992-bullhead-rev-101.dtb
# dtb-$(CONFIG_ARCH_QCOM)	+= msm8994-angler-rev-101.dtb
# dtb-$(CONFIG_ARCH_QCOM)	+= msm8996-mtp.dtb

ifeq ($(CONFIG_BUILD_ARM64_DT_OVERLAY),y)
# Only list overlays that have matching .dts sources and compile cleanly.
# Do not put comments with trailing backslashes inside the continued list;
# GNU make joins lines first, then strips # comments, which truncates the list.
#
# fajita-*-spec overlays omitted: DTC fails with duplicate label
# 'qnovo_fet_ctrl_default' when compiling those overlays.
dtbo-$(CONFIG_ARCH_QCOM) += \
	sdm845-mtp-overlay.dtbo \
	sdm845-v2-mtp-overlay.dtbo \
	sdm845-v2.1-mtp-overlay.dtbo \
	enchilada-dvt-v2.1-overlay.dtbo \
	enchilada-dvt-v2.1-backup-overlay.dtbo \
	enchilada-dvt-v2.1-usb30-overlay.dtbo \
	enchilada-pvt-v2.1-overlay.dtbo \
	enchilada-pvt-v2.1-backup-overlay.dtbo \
	enchilada-mp-v2.1-overlay.dtbo \
	fajita-pvt-v2.1-overlay.dtbo \
	fajita-pvt-v2.1-bu-overlay.dtbo \
	fajita-pvt-v2.1-v1-overlay.dtbo

sdm845-mtp-overlay.dtbo-base := sdm845.dtb
sdm845-v2-mtp-overlay.dtbo-base := sdm845-v2.dtb
sdm845-v2.1-mtp-overlay.dtbo-base := sdm845-v2.1.dtb
enchilada-dvt-v2.1-overlay.dtbo-base := sdm845-v2.1.dtb
enchilada-dvt-v2.1-backup-overlay.dtbo-base := sdm845-v2.1.dtb
enchilada-dvt-v2.1-usb30-overlay.dtbo-base := sdm845-v2.1.dtb
enchilada-pvt-v2.1-overlay.dtbo-base := sdm845-v2.1.dtb
enchilada-pvt-v2.1-backup-overlay.dtbo-base := sdm845-v2.1.dtb
enchilada-mp-v2.1-overlay.dtbo-base := sdm845-v2.1.dtb
fajita-pvt-v2.1-overlay.dtbo-base := sdm845-v2.1.dtb
fajita-pvt-v2.1-bu-overlay.dtbo-base := sdm845-v2.1.dtb
fajita-pvt-v2.1-v1-overlay.dtbo-base := sdm845-v2.1.dtb
else
dtb-$(CONFIG_ARCH_QCOM)	+= sdm845-mtp.dtb
endif

always		:= $(dtb-y)
subdir-y	:= $(dts-dirs)
clean-files    := *.dtb *.dtbo
