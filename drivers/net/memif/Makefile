# SPDX-License-Identifier: BSD-3-Clause
# Copyright 2018-2019 Cisco Systems, Inc.  All rights reserved.

include $(RTE_SDK)/mk/rte.vars.mk

#
# library name
#
LIB = librte_pmd_memif.a

EXPORT_MAP := rte_pmd_memif_version.map

LIBABIVER := 1

CFLAGS += -O3
CFLAGS += $(WERROR_FLAGS)
CFLAGS += -DALLOW_EXPERIMENTAL_API
# Experimantal APIs:
# - rte_intr_callback_unregister_pending
LDLIBS += -lrte_eal -lrte_mbuf -lrte_mempool
LDLIBS += -lrte_ethdev -lrte_kvargs
LDLIBS += -lrte_hash
LDLIBS += -lrte_bus_vdev

#
# all source are stored in SRCS-y
#
SRCS-$(CONFIG_RTE_LIBRTE_PMD_MEMIF) += rte_eth_memif.c
SRCS-$(CONFIG_RTE_LIBRTE_PMD_MEMIF) += memif_socket.c

include $(RTE_SDK)/mk/rte.lib.mk
