---
title: ترقية دفاتر يومية الإيصالات الفردية وعمليات إعادة تقييم العملة
description: يشرح هذا الموضوع كيفية ترقية دفاتر يومية الإيصالات الفردية وعمليات إعادة تقييم العملة.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 6b66b969d13cff7f1f39fb644f459aa92bea198f
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743911"
---
# <a name="upgrade-single-voucher-journals-and-currency-revaluations"></a><span data-ttu-id="55732-103">ترقية دفاتر يومية الإيصالات الفردية وعمليات إعادة تقييم العملة</span><span class="sxs-lookup"><span data-stu-id="55732-103">Upgrade single-voucher journals and currency revaluations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="55732-104">تُدخل بعض المؤسسات دفاتر يومية تحتوي على إيصال واحد يشتمل على أكثر من عميل أو مورد واحد، كما تُجري عملية إعادة تقييم العملة الأجنبية للحسابات المدينة أو الحسابات الدائنة.</span><span class="sxs-lookup"><span data-stu-id="55732-104">Some organizations enter journals that contain a single voucher that has more than one customer or vendor, and they also run the Accounts receivable or Accounts payable foreign currency revaluation process.</span></span> <span data-ttu-id="55732-105">يصف هذا الموضوع الخطوات التي يجب على هذه المؤسسات اتباعها عند الترقية إلى الإصدار 1611 من Microsoft Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="55732-105">This topic describes the steps that these organizations should follow when they upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

<span data-ttu-id="55732-106">اتبع هذه الخطوات عند الترقية إلى الإصدار 1611 من Microsoft Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="55732-106">Follow these steps when you upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

1.  <span data-ttu-id="55732-107">قبل الترقية إلى Finance and Operations، شغّل عمليات إعادة تقييم العملة الأجنبية للحسابات المدينة والحسابات الدائنة.</span><span class="sxs-lookup"><span data-stu-id="55732-107">Before you upgrade to Finance and Operations, run the foreign currency revaluation processes for Accounts receivable and Accounts payable.</span></span> <span data-ttu-id="55732-108">عيّن الحقل **الطريقة** إلى **تاريخ الفاتورة**.</span><span class="sxs-lookup"><span data-stu-id="55732-108">Set the **Method** field to **Invoice date**.</span></span> <span data-ttu-id="55732-109">يتم إنشاء حركة إعادة تقييم تعكس عملية إعادة تقييم العملة الأجنبية الأخيرة.</span><span class="sxs-lookup"><span data-stu-id="55732-109">A revaluation transaction is created that reverses the last foreign currency revaluation.</span></span> <span data-ttu-id="55732-110">لذلك، يتم تقييم الحركات المفتوحة بعملة المحاسبة الأصلية الخاصة بها.</span><span class="sxs-lookup"><span data-stu-id="55732-110">Therefore, the open transactions are valued at their original accounting currency.</span></span>
2.  <span data-ttu-id="55732-111">الترقية إلى الإصدار 1611.</span><span class="sxs-lookup"><span data-stu-id="55732-111">Upgrade to version 1611.</span></span>
3.  <span data-ttu-id="55732-112">أجرِ عمليات إعادة تقييم العملة الأجنبية للحسابات المدينة والحسابات الدائنة مرة ثانية.</span><span class="sxs-lookup"><span data-stu-id="55732-112">Run the Accounts receivable and Accounts payable foreign currency revaluation processes again.</span></span> <span data-ttu-id="55732-113">في هذه المرة، عيّن **الطريقة** إلى **القياسية**.</span><span class="sxs-lookup"><span data-stu-id="55732-113">This time, set the **Method** field to **Standard**.</span></span> <span data-ttu-id="55732-114">يتم إنشاء حركة إعادة تقييم جديدة استناداً إلى أسعار الصرف الحالية.</span><span class="sxs-lookup"><span data-stu-id="55732-114">A new revaluation transaction is created that is based on the current exchange rates.</span></span> <span data-ttu-id="55732-115">تسجل هذه الحركة الأرباح/الخسائر غير المحققة وحساب دفتر الأستاذ للملخص الصحيح.</span><span class="sxs-lookup"><span data-stu-id="55732-115">This transaction records the unrealized gain/loss and the correct summary ledger account.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]