---
title: إضافة عملية حسابية إلى نموذج تكوين منتج
description: يوضح هذا الإجراء كيفية إضافة عملية حساب جديدة إلى نموذج تكوين منتج.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e703c6d505f1e2e77f454732301de7a6c130c58a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4421383"
---
# <a name="add-a-calculation-to-a-product-configuration-model"></a>إضافة عملية حسابية إلى نموذج تكوين منتج

[!include [banner](../../includes/banner.md)]

يوضح هذا الإجراء كيفية إضافة عملية حساب جديدة إلى نموذج تكوين منتج. ويُظهر كيف يمكنك إنشاء تعبير منطقي باستخدام العامل "لو" لتعيين ارتفاع مكبر الصوت إلى 10 لمكبرات الصوت البيضاء و15 لألوان الكابينات الأخرى. يستخدم الإجراء المكون مكبر الصوت المتطور في شركة العرض التوضيحي USMF.


## <a name="add-a-calculation"></a>إضافة عملية حساب

## <a name="create-calculation-expression"></a>إنشاء عملية تعبير حساب
1. انقر فوق "تحرير التعبير".
2. في الحقل "ConstraintBody"، أدخل "If[CabinetFinish=="White", 10, 15]".
3. انقر فوق "التحقق من الصحة‬".
4. انقر فوق "إغلاق".
5. انقر فوق "موافق".

