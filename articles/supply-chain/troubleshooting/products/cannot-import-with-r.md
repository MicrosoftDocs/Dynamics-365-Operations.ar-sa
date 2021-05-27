---
title: لا يمكن استيراد أحد الأصناف باستخدام الكيان المنتجات الصادرة V2
description: لا يمكن استيراد أحد الأصناف باستخدام الكيان المنتجات الصادرة V2.
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended, DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 8182f2f83f6a3e4cf54fe6fa64b25a2f461ff541
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026227"
---
# <a name="you-cant-import-an-item-by-using-the-released-products-v2-entity"></a><span data-ttu-id="ed096-103">لا يمكن استيراد أحد الأصناف باستخدام الكيان المنتجات الصادرة V2</span><span class="sxs-lookup"><span data-stu-id="ed096-103">You can't import an item by using the Released products V2 entity</span></span>

<span data-ttu-id="ed096-104">رقم KB: 4611825</span><span class="sxs-lookup"><span data-stu-id="ed096-104">KB number: 4611825</span></span>

## <a name="symptoms"></a><span data-ttu-id="ed096-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="ed096-105">Symptoms</span></span>

<span data-ttu-id="ed096-106">عند محاولة استيراد أحد الأصناف باستخدام الكيان *المنتجات الصادرة V2*، تظهر رسالة خطأ مشابهة للمثال التالي:</span><span class="sxs-lookup"><span data-stu-id="ed096-106">When you try to import an item by using the *Released products V2* entity, you receive an error message that resembles the following example:</span></span>

> <span data-ttu-id="ed096-107">لا يمكن إنشاء سجل في الأصناف - مجموعات أبعاد التعقب‬ (EcoResTrackingDimensionGroupItem).</span><span class="sxs-lookup"><span data-stu-id="ed096-107">Cannot create a record in Items - tracking dimension groups (EcoResTrackingDimensionGroupItem).</span></span> <span data-ttu-id="ed096-108">رقم الصنف: 2040663، الدفعة.</span><span class="sxs-lookup"><span data-stu-id="ed096-108">Item number: 2040663, Batch.</span></span> <span data-ttu-id="ed096-109">السجل موجود بالفعل.</span><span class="sxs-lookup"><span data-stu-id="ed096-109">The record already exists.</span></span>

## <a name="resolution"></a><span data-ttu-id="ed096-110">الدقة</span><span class="sxs-lookup"><span data-stu-id="ed096-110">Resolution</span></span>

<span data-ttu-id="ed096-111">لاستيراد منتجات صادرة جديدة، فإنه يجب استخدام الكيان *إنشاء المنتج الصادر V2* بدلاً من الكيان *المنتجات الصادرة V2*.</span><span class="sxs-lookup"><span data-stu-id="ed096-111">To import new released products, you must use the *Released product creation V2* entity instead of the *Released products V2* entity.</span></span>
